# Post data deployment updates for R5.x

Execute the following DML to update existing data in `testdef` and `testplantask` for the `instrumentterminal` column.

```
update intdsgndata.testspec ts set instrumentterminal = src.instrumentterminal
from(
SELECT 
  ts.id,
  STRING_AGG(i.instrumentterminal, ',' ORDER BY i.instrumentterminal) AS instrumentterminal
FROM 
  intdsgndata.testspec ts
JOIN 
  intdsgndata.v_instrument i 
  ON i.measurementlibcmdid = ts.measurementlibcmdid
WHERE 
  ts.equipmenttypeid = (
    SELECT id 
    FROM intdsgndata.equipmenttype e 
    WHERE e.testscripttype = 'NON'
  )
GROUP BY 
  ts.id
) src where src.id = ts.id 
; 

update intdsgndata.testplantask t set instrumentterminal = src.instrumentterminal
from(
select ts.id, ts.instrumentterminal from intdsgndata.testspec ts
) src where src.id = t.testspecid  
;

```

**Parent topic:**[Data deployment](../../id_docs/installation/data_deploy.md)

