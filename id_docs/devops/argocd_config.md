# Configure ArgoCD

If you’re using a private repository for the Helm chart or Kubernetes manifests, you must set it up under the ArgoCD repository settings.

To simplify configuration, it is recommended to set up a credential template which applies to many repositories under an organization, rather than setting up a repository for every single individual repository.

1.  Set up Repository certificates/known hosts.

    If you are using a private repository, add the public TLS certificate or SSH keys for the repository so it is trusted by ArgoCD. You can easily obtain the public key \(known hosts\) via the `ssh-keyscan` utility.

    **Example:**

    ```
    $ ssh-keyscan github.ibm.com
    
    # github.ibm.com:22 SSH-2.0-babeld-440c974
    github.ibm.com ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQC1K6pnwsCh8hFCqvzWkb1y3ajXervgfokIdZ/VIURIItVBIINtH5Ynupt2cLLBMYysYjR1I/P4VNZf7bX+HejjJqMf92psXQ1VToyKeNZ+i01CrhZko11157veidnMwVmKoCIdrKpsLgqthJ6kXLrTqaVIQ1sh3lKZ0tFRsqgiwNbstwhRZe/MyUoDuzHZQPooxsiy5dBO+LpkovCShwVfZ3380UyAfScPrUZcX2zY/qmGDz4puXOWj/CQupoe76JoVenfwrjfTw2I+GoPxpZK6R47akoAekCO+Dw8VW4NnTDR6L7eGkclltQSC7HQ9MiFDB4Z49ONWQwotLdttDr5
    # github.ibm.com:22 SSH-2.0-babeld-440c974
    github.ibm.com ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBC1Sg96+K5rc8ZTYhidXI1Q6qUBRgrC51I2pUop4xo4keH8r/5V1W+z2dZNKZsVLW12ulIAe9yorXt2MrI8V0XE=
    # github.ibm.com:22 SSH-2.0-babeld-440c974
    # github.ibm.com:22 SSH-2.0-babeld-440c974
    # github.ibm.com:22 SSH-2.0-babeld-440c974
    ```

    Paste these keys into ArgoCD when adding an SSH Known Host. Substitute IBM’s GitHub server with your own.

2.  Add a cluster.

    You can use the default entry when controlling the cluster ArgoCD is installed on.

3.  Create Projects.

    You can create different projects to logically separate different applications or environments. One example might be to separate test and production environments into different Projects. You should create a Project for the Intelligent Design application. When creating a Project, be sure to set the scoped repositories to either a catch-all/wildcard or include all the repositories needed to deploy the application. The local cluster \(or wildcard\) should also be set in the allowed destinations list.


