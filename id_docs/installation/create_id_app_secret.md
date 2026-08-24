# Creating and updating the Intelligent Design application secret

The Helm chart supports using either a single secret to store the credentials it requires, or multiple secrets can be specified throughout the Values file.

The following example shows using a single secret.

Create/Update a new secret which contains the following keys:

```
kind: Secret
apiVersion: v1
metadata:
  name: intldsgn-secrets
data:
  config.username: (1)
  config.password: (2)
  spring.datasource.url: (3)
  spring.datasource.username: (4)
  spring.datasource.password: (5)
  nextAuth.secret: (6)
  keycloak.adminClientSecret: (7)
  keycloak.baseFrontendSecret: (8)
  keycloak.testFrontendSecret: (9)
  keycloak.ptcFrontendSecret: (10)
type: Opaque

```

1.  Username microservices are used to authenticate with the config service to obtain data source and configuration information. This is arbitrary and can be generated.
2.  Password microservices are used to authenticate with the config service to obtain data source and configuration information. This is arbitrary and can be generated.
3.  Datasource URL for the Postgres database server. This should be in connection string form, e.g. `jdbc:postgresql://<db_url>:5432/intldsgn_config?currentSchema=systemconfig`
4.  Username for the database `user/role`
5.  Password for the database `user/role`
6.  Random seed string used to encrypt data for NextJS user interface. This can be generated with the following command: `openssl rand -base64 32`
7.  Keycloak client secret for the user manager \(required if user manager enabled\).
8.  Keycloak client secret for the base user interface.
9.  Keycloak client secret for the test frontend \(required if test frontend enabled\).
10. Keycloak client secret for the post-test calculation frontend \(required if PTC frontend enabled\).

