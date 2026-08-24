# PTC Admin and User Role Permissions

In the Intelligent Design application, user roles define user permissions. Each user has a defined set of permissions that allow or restrict the configuration actions an ID user can take. The Post Test Calculation application has its own set of permissions for PTC Admin and PTC User roles.

You must add users to one of these role groups during the PTC setup to grant access to the following configuration actions. For more information, see [Assigning a user to a group](../installation/assign_user_to_group.md).

**Tip:** You can enter the necessary URI\(s\) when you create the feature keys in [Application Management](../admin/app_management.md).

|Feature Key|Description \(User Action\)|URI\(s\)|PTC Admin Role|PTC User Role|
|-----------|---------------------------|--------|--------------|-------------|
|TestDataView|Viewing test data\(all: chip-level, wafer-level, lot-level, and TEDS-level\)|```
/api/v1/ptc/testdata/test/metadata 
/api/v1/ptc/testdata/lot/{lotid}/summary 
/api/v1/ptc/testdata/lot/{lotid}/wafer/{waferid}/summary
/api/v1/ptc/testdata/lot/{lotid}/wafer/{waferid}/pnp/{pnp}/summary
/api/v1/ptc/testdata/lot/{lotid}/wafer/{waferid}/parametersummary
/api/v1/ptc/testdata/pnp/{pnp}/lot/{lotid}/wafer/{waferid}/measurements 
/api/v1/ptc/testdata/technology 
/api/v1/ptc/testdata/technologies 
/api/v1/ptc/testdata/lot/{lotid}
/api/v1/ptc/testdata/testlevels

```

|X|X|
|ReloadData|Reloading/processing test data|```
/api/v1/ptc/recalculation/technology/{tech}/teds/lotpnps
/api/v1/ptc/recalculation/create
/api/v1/ptc/recalculation/jobs
/api/v1/ptc/recalculation/ifdw/enabled
```

|X|X|
|SpecificationView|Viewing specifications|```
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/specs
```

|X|X|
|SpecificationEdit|Editing/creating Specifications|```
 
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/specs/update
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/screens/create
/api/v1/ptc/speccalc/technology/{tech}/pnpdetails
/api/v1/ptc/speccalc/technology/{tech}/units


```

|X|X|
|CalculationView|Viewing calculated parameters|```
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/calculations 
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/csv
```

|X|X|
|CalculationEdit|Editing Calculated Parameters|```
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/calculations/update/{calcid}
```

|X|X|
|CalculationCreate|Creating calculated parameters|```
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/calculations/create 
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/csv/update 
/api/v1/ptc/speccalc/validate/expression 
/api/v1/ptc/speccalc/technology/{tech}/pnps 
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/parameternames
```

|X|X|
|CalculationDelete|Delete calculated parametrs|```
/api/v1/ptc/speccalc/technology/{tech}/pnp/{pnp}/calculations/delete/{calcid}
```

|X|X|
|WaferDispositionView|View wafer disposition rules|```
/api/v1/ptc/waferdisposition/wafer/{waferid}
/api/v1/ptc/waferdisposition/technology/{tech}/pnp/{pnp}

```

|X|X|
|WaferDispositionEdit|Edit wafer disposition rule|```
/api/v1/ptc/waferdisposition/technology/{tech}/pnp/{pnp}/update/{wafdispoid}
```

|X|X|
|WaferDispositionCreate|Create wafer disposition rule|```
/api/v1/ptc/waferdisposition/technology/{tech}/pnp/{pnp}/create
```

|X|X|
|WaferDispositionDelete|Delete wafer disposition rule|```
/api/v1/ptc/waferdisposition/delete/{waferdispoid}
```

|X|X|
|LotDispositionView|View lot disposition rules|```
/api/v1/ptc/lotdisposition/lot/{lotid} 
/api/v1/ptc/lotdisposition/exists 
/api/v1/ptc/lotdisposition/family_codes
```

|X|X|
|LotDispositionEdit|Edit lot disposition rules|```
/api/v1/ptc/lotdisposition/update/{lotdispoid}
```

|X|X|
|LotDispositionCreate|Create lot disposition rules|```
/api/v1/ptc/lotdisposition/technology/{tech}/create
```

|X|X|
|LotDispositionDelete|Delete lot disposition rules|```
/api/v1/ptc/lotdisposition/delete/{lotdispoid}
```

|X|X|
|SFTPManage|Read and Update SFTP send to ISDW|```
/api/v1/ptc/admin/sftp 
/api/v1/ptc/admin/sftp/update 
/api/v1/ptc/admin/cachereset
```

|X||
|SiViewManage|Read and Update SiView connection information|```
/api/v1/ptc/admin/siview 
/api/v1/ptc/admin/siview/update
```

|X||
|UserPreferencesManage|Manage User Preferences/bookmarks etc|```

/api/v1/ptc/user/prefs
/api/v1/ptc/user/prefs/create
/api/v1/ptc/prefs/bookmarks
/api/v1/ptc/prefs/recently/viewed
/api/v1/ptc/prefs/filters
/api/v1/ptc/prefs/filters/update
/api/v1/ptc/prefs/filters/current
/api/v1/ptc/prefs/filters/current/update
/api/v1/ptc/prefs/filters/views
/api/v1/ptc/prefs/filters/bookmarks

```

|X|X|

**Parent topic:**[Post Test Calculation deployment](../../id_docs/post_test_calc/ptc_deploy_overview.md)

