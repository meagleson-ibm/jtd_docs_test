# Custom Pipelines

The Intelligent Design development Pipelines are build on Tekton \(OpenShift Pipelines implementation\). Depending on the source code and format there are several currently implemented pipelines which can build and deploy code.

**Java**

-   java-build-package - builds Java application code and packages into a container

    ![Java build package](../_images/java-build-package.png)

-   mvn-deploy-script - builds Java code \(libraries\) and POMs, uploads to GitHub repository

    ![mvn deploy script](../_images/mvn-deploy-script.png)


****

-   nodejs-build-libs - builds NodeJS libraries and uploads to GitHub repository

    ![NodeJS build libs](../_images/nodejs-build-libs.png)

-   nodejs-build-package - builds NodeJS web application code and packages into a container

    ![NodeJS build package](../_images/nodejs-build-package.png)


**Generic**

-   build-container - builds a customized image from a Dockerfile, no special pre or post-processing

    ![generic build container](../_images/build-container.png)


