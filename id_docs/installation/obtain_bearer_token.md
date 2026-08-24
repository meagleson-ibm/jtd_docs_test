# Obtaining a Bearer token

1.  Call Keycloak API.

    The following code is an example. Replace the URL and \{ \} parameters with appropriate values.

    ```
    curl --location 'https://intldsgnkeycloak.
    apps.id1.sde.sample.com/realms/intldsgn/protocol/openidconnect/token' \
    --header 'Content-Type: application/x-www-form-urlencoded' \
    --data-urlencode 'client_id=id-application-client' \
    --data-urlencode 'username={Project Administrator User}' \
    --data-urlencode 'password={password}' \
    --data-urlencode 'grant_type=password' \
    --data-urlencode 'client_secret={client secret}'
    ```

2.  Obtain the `access_token` value, such as in the following example.

    ```
    eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJOVHJrTVhTT29IWW92dz
    BKVnZnZi16aktueVFDdW1uUUtVTGp2M2J5LUxRIn0.eyJleHAiOjE3NDU4NDEwOTIsImlh
    dCI6MTc0NTc5Nzg5MiwianRpIjoiYWNjZDQ4MDEtNzRjNy00NDk0LThlMjktOWJlMzYxOW
    QyM2ZlIiwiaXNzIjoiaHR0cHM6Ly9pbnRsZHNnbi1sb2dpbi5hcHBzLmlkMS5zZGUuaWJt
    LmNvbS9yZWFsbXMvaW50bGRzZ24iLCJhdWQiOiJhY2NvdW50Iiwic3ViIjoiOGRkM2QwYz
    EtNTJiMi00YThiLThhYjktYzg3MTRhNWEzMzRjIiwidHlwIjoiQmVhcmVyIiwiYXpwIjoi
    aWQtYXBwbGljYXRpb24tY2xpZW50Iiwic2Vzc2lvbl9zdGF0ZSI6IjRkMGI4OGUyLTc4Zm
    QtNDQ4Ny04NzExLWIzMWUwMTg1MWRlYyIsImFjciI6IjEiLCJhbGxvd2VkLW9yaWdpbnMi
    OlsiaHR0cHM6Ly9pbnRsZHNnbi5hcHBzLmlkMS5zZGUuaWJtLmNvbS8iXSwicmVhbG1fYW
    NjZXNzIjp7InJvbGVzIjpbIlByb2plY3QgQWRtaW5pc3RyYXRvciIsIm9mZmxpbmVfYWNj
    ZXNzIiwidW1hX2F1dGhvcml6YXRpb24iLCJkZWZhdWx0LXJvbGVzLWludGxkc2duIl19LC
    JyZXNvdXJjZV9hY2Nlc3MiOnsiYWNjb3VudCI6eyJyb2xlcyI6WyJtYW5hZ2UtYWNjb3Vu
    dCIsIm1hbmFnZS1hY2NvdW50LWxpbmtzIiwidmlldy1wcm9maWxlIl19fSwic2NvcGUiOi
    Jwcm9maWxlIGVtYWlsIiwic2lkIjoiNGQwYjg4ZTItNzhmZC00NDg3LTg3MTEtYjMxZTAx
    ODUxZGVjIiwiZW1haWxfdmVyaWZpZWQiOnRydWUsIm5hbWUiOiJWYWxlcmllIEJhY2FsZX
    IiLCJwcmVmZXJyZWRfdXNlcm5hbWUiOiJ2YWxlcmllLmJhY2VsZXJAZXhhbXBsZS5jb20i
    LCJnaXZlbl9uYW1lIjoiVmFsZXJpZSIsImZhbWlseV9uYW1lIjoiQmFjYWxlciIsImVtYW
    lsIjoidmFsZXJpZS5iYWNlbGVyQGV4YW1wbGUuY29tIn0.fSWJx-
    MkhPXzl9CS4lt0Li2L2XhNb4K6H_Uumbag6unXmgwtU3cLYJCX4C9ABa1UAK8QfcPuCzNwcLfyq9XYQRehTtRA3kUm3T7H95pAugnb6gscrQ36fEMcAaz
    WfrEzFyzbWD6-ztffpUD1oWE5U1o7gBBGUgp69hEK1wtJlBcPeOQLK1fAmwCUk2m93Vgq4sXKYjaWJq3-
    tpZCSa_ME6zArcSQvFuxEAI1EzfON02OWrBkDyVf8iybwHuWfckba5CC8y7cAbW6LtEmJVtwuORUzB0Oe2PWGECyvdks2oi4I7ghDyQ-
    yEQidwM1KskjDTmX4DkqWWCHvcEU6Q
    /
    ```


**Parent topic:**[Post data migration steps](../../id_docs/installation/post_migration_steps.md)

