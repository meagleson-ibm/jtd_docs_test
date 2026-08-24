# Tasks

-   ****git-clone** - performs a git clone into a mounted workspace**

    Key Parameters:

    -   url - Repository URL to clone from
    -   revision - Revision to checkout. \(branch, tag, sha, ref, etc…\)
    Results:

    -   commit - The precise commit SHA that was fetched by this Task
    -   url - The precise URL that was fetched by this Task
    -   committer-date - The epoch timestamp of the commit that was fetched by this Task
    -   committer-name - The author of the commit that was fetched by this Task
    -   commit-msg - The message of the commit that was fetched by this Task
    -   sonar-properties-present- if SonarQube sonar-project.properties is present

-   ****maven-wrapper** - Calls Maven with wrapper \(./mvnw\), typically used to build .jar files**

    Key Parameters:

    -   GOALS - maven goals to run
    -   MAVEN\_ARGS - optional arguments to pass to maven process

-   ****sonarqube-scanner** - Runs Sonar CLI for static code analysis**

    Key Parameters:

    -   SONAR\_HOST\_URL - SonarQube server URL
    -   SONAR\_PROJECT\_KEY - Project’s unique key
    -   SONAR\_SCANNER\_IMAGE - The sonarqube scanner CLI image which will run the scan
    -   SONAR\_TOKEN - SonarQube user authentication token
    -   QUALITY\_GATE\_CHECK - Fail Pipeline when Quality Check fails
    Results:

    -   quality\_gate - The status of the SonarQube quality gate check
    -   project\_url - The URL to the SonarQube scan result

-   ****build-image** - build docker container using buildah**

    Key Parameters:

    -   IMAGE - Reference of the image buildah will produce
    -   DOCKERFILE - Path to the Dockerfile to build
    -   BUILD\_EXTRA\_ARGS - Extra parameters passed for the build command when building images
    Results:

    -   IMAGE\_DIGEST - Digest of the image just built
    -   IMAGE\_URL - Image repository where the built image would be pushed to

-   ****update-manifests** - Run Renovatebot to update dependencies/manifests**

-   ****send-slack-webhook** - Send webhook to Slack to report build status**

    Key Parameters:

    -   WEBHOOK\_URL - Secret name of slack webhook URL \(key = url\)
    -   BASE\_URL - Base URL of OpenShift environment for Slack notification links
    -   TASKS\_STATUS - Aggregate status/results of the pipeline tasks
    -   PIPELINERUN\_NAME - Name of the PipelineRun to report
    -   COMMITTER\_NAME - Name of the committer of the commit revision being built
    -   COMMITTER\_DATE - Date of the commit revision being built
    -   COMMIT - Commit SHA of the revision being built
    -   COMMIT\_MSG - message of the commit of the revision being built
    -   QUALITY\_GATE\_CHECK - whether or not the quality gate is being enforced
    -   SONARQUBE\_STATUS - whether or not the code passed the Sonar quality check

-   ****npm** - used to run npm goals on a project \(usually clean-install, test, or build\)**

    Key Parameters:

    -   ARGS - The npm goals you want to run
    -   IMAGE - The node image you want to use

-   ****push-artifacts****

    Key Parameters:

    -   GIT\_REPO - Git repository of library source
    -   GIT\_USER\_NAME - Git user name for performing git operation
    -   GIT\_USER\_EMAIL - Git user email for performing git operation

