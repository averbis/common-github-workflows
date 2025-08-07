# Reusable GitHub Workflows

For project that do not have special build requirements, it is tedious to maintain workflows - in particular when they need to be upgraded.
For such projects, it is recommended to defer to our standard workflows. 
This repository contains the standard workflows in `.github/workflows` as well as examples of how to call those:

* [`example-maven-ci-build.yml`](example-maven-ci-build.yml): Example for calling the [Standard Maven CI workflow](.github/workflows/maven-ci-build.yml)
* [`example-maven-release-build.yml`](example-maven-release-build.yml): Example for calling the [Standard Maven Release workflow](.github/workflows/maven-release-build.yml)

To use these examples in your repository:

* create a older `.github/workflows` in the repository
* copy the example workflows into that directory (remove the `example-` prefix from the file name)
* either
  * comment out the `paths-ignore: [ ".github/**" ]` line and create a PR with the changes
  * or commit the changes to your main branch and manually trigger a build via **Actions** -> **Java CI Build** -> **Dispatch**
