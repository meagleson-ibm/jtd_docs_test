# Configuration Management User Role Permissions

In the Intelligent Design application, user roles define user permissions. Each user has a defined set of permissions that allow or restrict the configuration actions an ID user can take. The Configuration Management component in Intelligent Test has its own set of permissions for Administrator, Tester, and Test Engineer Admin roles.

**Tip:** You can enter the necessary URI\(s\) when you create the feature keys in [Application Management](app_management.md).

|Feature Key|Description \(User Action\)|URI\(s\)|Project Administrator|Tester|Test Engineer Administrator|
|-----------|---------------------------|--------|---------------------|------|---------------------------|
|ConfigurationManagement|Required for view access| |X|X|X|
|AlgorithmImport|Import Algorithm \(Measurement Lib Cmd\)|```
/api/v1/abls/testingresource/equipment/measurementlibcmd/preview
/api/v1/abls/testingresource/equipment/measurementlibcmd/bulk-save
```

| |X|X|
|EquipmentDelete|Deletes Equipment its libraries and their algorithms|```
/api/v1/abls/testingresource/equipment/type/{id}/delete
```

|X|X|X|
|EquipmentCreate|Creates Equipment|```
/api/v1/abls/testingresource/equipment/type/save
```

|X|X|X|
|LibraryDelete|Deletes Library and their algorithms|```
/api/v1/abls/testingresource/equipment/lib/{id}/delete
```

|X|X|X|
|LibraryCreate|Creates Libraries|```
/api/v1/abls/testingresource//equipment/lib/save
```

|X|X|X|
|ProbeCreate|Create Probe|```
/api/v1/abls/testingresource/equipment/probe/save
```

| |X|X|
|ProbeEdit|Edit - Update Probe|```
/api/v1/abls/testingresource/equipment/probe/save
```

| |X|X|
|ProbeView|View Probe|```
/api/v1/abls/testingresource/equipment/probe/{id}/get
```

| |X|X|
|ProbeDelete|Delete Probe|```
/api/v1/abls/testingresource/equipment/probe/{id}/delete
```

| |X|X|
|ProbeDownload|Download Probe|```

```

| | | |
|AspectAdd| |```

```

|X|X|X|
|AssetCreate|Create Asset|```
/api/v1/abls/testingresource/asset/save
```

| |X|X|
|AssetEdit|Edit - Update Asset|```
/api/v1/abls/testingresource/asset/save
```

| |X|X|
|AssetCopy|Copy Asset|```
/api/v1/abls/testingresource/asset/{id}/copy
```

| |X|X|
|AssetArchive|Archive Asset|```
/api/v1/abls/testingresource/asset/archivedstatus
```

| |X|X|
|AssetRestore|Restore asset\(s\)|```

```

| | | |
|AssetDownload|Download Asset|```
/api/v1/abls/testingresource/asset/export
```

| |X|X|
|AssetDelete|Delete Asset|```
api/v1/abls/testingresource/asset/delete
```

| |X|X|

**Parent topic:**[ID User Role Permissions](../../id_docs/admin/id_user_role_permissions.md)

