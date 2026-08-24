# Deploying Intelligent Design data repositories

1.  Extract the Deployment Package .tar file to create the intldsgn-data-application folder.

2.  Save the extracted folder on your local machine.

3.  Verify the pom.xml configuration.

    Ensure that the pom.xml file contains:

    -   Correct Maven profile name
    -   Correct database connection details
    -   Proper Liquibase properties
    1.  POM for Intelligent Design Database deployment: In pom.xml, update the following for Intelligent Design deployment:

        -   **Profile:** e.g., id-prod
        -   **Execution Name:** meaningful and environment specific
        -   **Database Credentials:** URL, username, password for ID database
        -   **Liquibase Context \(As Is\):** `<contexts>${liquibase.contexts}</contexts>`
    2.  POM for PTC Database deployment: In pom.xml, update the following for Intelligent Design deployment:

        -   **Profile:** e.g., ptc-prod
        -   **Execution Name:** meaningful and environment specific
        -   **Database Credentials:** URL, username, password for PTC database
        -   **Liquibase Context \(As Is\):** `<contexts>${liquibase.contexts}</contexts>`
    See [POM template \(reference\)](pom_template_ref.md).

4.  Execute the following command only if the PTC database is separated from the ID database, and all PTC scripts were executed manually up until R6.0 \(without Liquibase maven command\):

    `SET my.lb_schema = public;` \(If you want to force a schema other than changelog schema.\)

    ```
    BEGIN;
    
    DO $$
    DECLARE
      v_schema text;
    BEGIN
      -- A) explicit override
      v_schema := current_setting('my.lb_schema', true);
    
      IF v_schema IS NULL OR btrim(v_schema) = '' THEN
        -- B) prefer 'changelog' schema if it exists
        IF EXISTS (SELECT 1 FROM pg_namespace WHERE nspname = 'changelog') THEN
          v_schema := 'changelog';
        ELSE
          -- C) fallback to whatever resolves as current_schema()
          v_schema := current_schema();
        END IF;
      END IF;
    
      -- Ensure schema exists (safe even if it already exists)
      EXECUTE format('CREATE SCHEMA IF NOT EXISTS %I', v_schema);
    
      -- Route unqualified object names to the chosen schema for this transaction
      PERFORM set_config('search_path', format('%I, public', v_schema), true);
    
      RAISE NOTICE 'Using Liquibase metadata schema: %', v_schema;
    END $$;
    
    
    --------------------------------------------------------------------------------
    -- 1) Create DATABASECHANGELOGLOCK (if missing)
    --------------------------------------------------------------------------------
    CREATE TABLE IF NOT EXISTS databasechangeloglock (
      id          INTEGER NOT NULL,
      locked      BOOLEAN NOT NULL,
      lockgranted TIMESTAMP WITHOUT TIME ZONE,
      lockedby    VARCHAR(255),
      CONSTRAINT pk_databasechangeloglock PRIMARY KEY (id)
    );
    
    -- Liquibase expects a single row with id=1
    INSERT INTO databasechangeloglock (id, locked, lockgranted, lockedby)
    VALUES (1, FALSE, NULL, NULL)
    ON CONFLICT (id) DO NOTHING;
    
    --------------------------------------------------------------------------------
    -- 2) Create DATABASECHANGELOG (if missing)
    -- Note: This matches common Liquibase 4.x structure for PostgreSQL.
    --------------------------------------------------------------------------------
    CREATE TABLE IF NOT EXISTS databasechangelog (
      id             VARCHAR(255) NOT NULL,
      author         VARCHAR(255) NOT NULL,
      filename       VARCHAR(255) NOT NULL,
      dateexecuted   TIMESTAMP WITHOUT TIME ZONE NOT NULL,
      orderexecuted  INTEGER NOT NULL,
      exectype       VARCHAR(10) NOT NULL,
      md5sum         VARCHAR(35),
      description    VARCHAR(255),
      comments       VARCHAR(255),
      tag            VARCHAR(255),
      liquibase      VARCHAR(20),
      contexts       VARCHAR(255),
      labels         VARCHAR(255),
      deployment_id  VARCHAR(10)
    );
    
    -- Enforce "insert only if (id,author,filename) doesn't exist"
    -- Works even if table already exists (and prevents duplicates under concurrency)
    CREATE UNIQUE INDEX IF NOT EXISTS uq_databasechangelog_id_author_filename
      ON databasechangelog (id, author, filename);
    
    --------------------------------------------------------------------------------
    -- 3) Insert rows only when the (id, author, filename) combination doesn't exist
    --------------------------------------------------------------------------------
    INSERT INTO databasechangelog
    (id, author, filename, dateexecuted, orderexecuted, exectype, md5sum, description, comments, tag, liquibase, contexts, labels, deployment_id)
    VALUES
    ('v.2.2.0', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:35:45.914', 1, 'EXECUTED', '8:05725b6c6607ae7bf65545809c7ca834', 'tagDatabase', '', 'v.2.2.0', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1645.sql', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:36:19.999', 2, 'EXECUTED', '8:72c1e5d719e854192fdf6531cec8105f', 'sqlFile', 'DDL_Script_Jira_INTED-1645', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1712.sql', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:36:58.541', 3, 'EXECUTED', '8:7111b9e79d93e1060077929c2f398ad4', 'sqlFile', 'DDL_Script_Jira_INTED-1712', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1721.sql', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:37:00.090', 4, 'EXECUTED', '8:069948e514def431f6067fc960b86a9a', 'sqlFile', 'DDL_Script_Jira_INTED-1721', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1804.sql', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:37:03.099', 5, 'EXECUTED', '8:445f25b112f05c42bb432370db53848e', 'sqlFile', 'DDL_Script_Jira_INTED-1804', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1812.sql', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:37:05.109', 6, 'EXECUTED', '8:45f634ed0797b38becd169d16f560ee8', 'sqlFile', 'DDL_Script_Jira_INTED-1812', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.2.1', 'balaji.ramamurthy@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:37:05.832', 7, 'EXECUTED', '8:4133ba4a3f8f89a298b9f635a560acbb', 'tagDatabase', '', 'v.2.2.1', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-1819.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.2/releaselog.xml', '2026-02-04 18:37:08.031', 8, 'EXECUTED', '8:f9148647471a0b98d491bde9655b3845', 'sqlFile', 'DDL_Script_Jira_INTED-1819', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.2.1', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.2.1/releaselog.xml', '2026-02-04 18:37:08.796', 9, 'EXECUTED', '8:4133ba4a3f8f89a298b9f635a560acbb', 'tagDatabase', '', 'v.2.2.1', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2143_A.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.2.1/releaselog.xml', '2026-02-04 18:37:10.291', 10, 'EXECUTED', '8:da4b769df853b90ded52165407ddb2d6', 'sqlFile', 'DDL_Script_Jira_INTED-2143_A', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2143.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.2.1/releaselog.xml', '2026-02-04 18:37:18.588', 11, 'EXECUTED', '8:c107a41ae2375182832b428706e8601a', 'sqlFile', 'DDL_Script_Jira_INTED-2143', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2143_B.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.2.1/releaselog.xml', '2026-02-04 18:37:20.367', 12, 'EXECUTED', '8:6063c10cb4006802562d81835e384821', 'sqlFile', 'DDL_Script_Jira_INTED-2143_B', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.3', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:21.188', 13, 'EXECUTED', '8:d3c799218881c1d6693d1b8071142f2f', 'tagDatabase', '', 'v.2.3', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2190.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:30.640', 14, 'EXECUTED', '8:903039946dded0b4af1a3aac6c583458', 'sqlFile', 'DDL_Script_Jira_INTED-2190', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.3.1', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:31.337', 15, 'EXECUTED', '8:beff75c05c8982cafa97c4b3cbdb213c', 'tagDatabase', '', 'v.2.3.1', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2231_A.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:32.766', 16, 'EXECUTED', '8:a0e2173580fbc33095a91da36fbaf690', 'sqlFile', 'DDL_Script_Jira_INTED-2231_A', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2231.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:42.325', 17, 'EXECUTED', '8:903039946dded0b4af1a3aac6c583458', 'sqlFile', 'DDL_Script_Jira_INTED-2231', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2231_B.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:44.905', 18, 'EXECUTED', '8:5efd2991c7025cb7366778b77ac4ce1e', 'sqlFile', 'DDL_Script_Jira_INTED-2231_B', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.3.2', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:45.600', 19, 'EXECUTED', '8:ef6975540cd0b03bdc183cabf76bab0b', 'tagDatabase', '', 'v.2.3.2', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2236.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:47.335', 20, 'EXECUTED', '8:f26cf9ef19dbacc687e27ee63322e00a', 'sqlFile', 'DDL_Script_Jira_INTED-2236', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.2.3.3', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:48.046', 21, 'EXECUTED', '8:8864da517fc8a6001cbed5d53fc468f3', 'tagDatabase', '', 'v.2.3.3', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2271.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:37:52.082', 22, 'EXECUTED', '8:9f9c2d8d5522ce33f28e532361d68df4', 'sqlFile', 'DDL_Script_Jira_INTED-2271', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-2691.sql', 'balaji.ramamurthy1@ibm.com', 'src/main/resources/releases/INTED R2.3/releaselog.xml', '2026-02-04 18:38:00.414', 23, 'EXECUTED', '8:cc322dd5372f0a17771f9541d2f7d374', 'sqlFile', 'DDL_Script_Jira_INTED-2691', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.6.0.5', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:01.076', 24, 'EXECUTED', '8:a977f37d93e9596fa698c05865dafcc2', 'tagDatabase', '', 'v.6.0.5', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-3399.sql', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:02.966', 25, 'EXECUTED', '8:39a07c8e26fb0b7ce556dce9afb42772', 'sqlFile', 'DDL_Script_Jira_INTED-3399', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.6.0.8', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:03.788', 26, 'EXECUTED', '8:368772e733d960fd2969ee68dcd85718', 'tagDatabase', '', 'v.6.0.8', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-3449.sql', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:05.237', 27, 'EXECUTED', '8:eb9b38318b8487d021e4311e8ea45026', 'sqlFile', 'DDL_Script_Jira_INTED-3449', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.6.0.15', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:06.040', 28, 'EXECUTED', '8:40c85c2fee43759664a2b9c2a78378e4', 'tagDatabase', '', 'v.6.0.15', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-3611.sql', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.0/releaselog.xml', '2026-02-04 18:38:07.678', 29, 'EXECUTED', '8:aee9ef3f203d61d4fe7afe01042b4276', 'sqlFile', 'DDL_Script_Jira_INTED-3611', NULL, '4.8.0', 'ptc', NULL, '0210345022'),
    ('v.6.1.1', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.1/releaselog.xml', '2026-02-04 18:38:08.553', 30, 'EXECUTED', '8:5676eb86d370b534838c252cd2d82f68', 'tagDatabase', '', 'v.6.1.1', '4.8.0', 'ptc', NULL, '0210345022'),
    ('DDL_Script_Jira_INTED-3544.sql', 'sanjeetk@in.ibm.com', 'src/main/resources/releases/INTED R6.1/releaselog.xml', '2026-02-04 18:38:10.450', 31, 'EXECUTED', '8:5ea51be09641fab82b2e40ed875f8960', 'sqlFile', 'DDL_Script_Jira_INTED-3544', NULL, '4.8.0', 'ptc', NULL, '0210345022')
    ON CONFLICT (id, author, filename) DO NOTHING;
    
    COMMIT;
    
    ```

5.  In Command line, navigate to the directory that contains the pom.xml file, and run Database Deployment Commands.

    |Deployment type|Maven command|Example profile name|
    |---------------|-------------|--------------------|
    |Intelligent Design DB|`mvn install -P<PROFILE_NAME> "-Dliquibase.contexts=intldsgn"`|id-prod|
    |PTC DB|`mvn install -P<PROFILE_NAME> "-Dliquibase.contexts=ptc"`|ptc-prod|

    **Important notes:**

    -   Replace **<PROFILE\_NAME\>** with the actual profile ID configured in pom.xml.
    -   Script execution begins, and Liquibase applies changesets based on the context.
    -   On successful execution, Maven displays: **BUILD SUCCESS**.

-   **[POM template \(reference\)](../../id_docs/installation/pom_template_ref.md)**  


**Parent topic:**[Data deployment](../../id_docs/installation/data_deploy.md)

