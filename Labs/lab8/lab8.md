# Lab 8 - Splitting CI and CD

In this lab we are going to implement a build pipeline that creates versioned artifacts that can be used by multiple other release pipelines afterwards.

> You can publish and consume many different types of packages and artifacts with Azure Pipelines. Your continuous integration/continuous deployment (CI/CD) pipeline can publish specific package types to their respective package repositories (NuGet, npm, Python, and so on). Or you can use build artifacts and pipeline artifacts to help store build outputs and intermediate files between build steps. You can then add onto, build, test, or even deploy those artifacts. Goto [docs.microsoft.com](https://docs.microsoft.com/azure/devops/pipelines/artifacts/artifacts-overview?view=azure-devops) to learn more.

Exercises:

* [8.1 Build Pipelines and Artifacts](#exercise-81-build-pipelines-and-artifacts)
* [8.2: Working with Build Artifacts](#exercise-82-working-with-build-artifacts)

---

## Exercise 8.1: Build Pipelines and Artifacts

Let us start with a build pipeline that creates and publishes build artifacts for us.

1. Goto Repos > Branches
1. Create a new branch "lab8" that is based on main
1. Goto Pipelines > Pipelines
1. Click on "New pipeline"
1. Click on "Azure Repos Git (YAML)"
1. Select our repository
1. Select "Existing Azure Pipelines YAML file"

    * Select the lab8 branch
    * Select `/.azdo/pipelines/build.pipeline.yml`

1. Click on "Continue"

    You will now see a very simple build pipeline that does two things:

    * Copy all files that end with *.sh (shell script)
    * Publish these files as build artifacts

    ![build pipeline example](img/010_build_pipeline_editor.png)

1. Click on "Run"
1. Click on "Job" to check the job details
1. Check the "CopyFiles" task

    You will see that our CopyFiles task found 1 file and copied it into out staging directory.

    ![build pipeline output](img/020_build_pipeline_output.png)

1. Next, check the "PublishPipelineArtifact" task

    You will see here that it has published 1 file. This is the file that was copied in the previous step.

    ![build pipeline output](img/030_build_pipeline_output2.png)

With this we have now successfully created a build pipeline that takes a subset of files from our repository and publishes them as artifacts.

You can also find your build artifacts from within the Azure DevOps UI when you goto the pipeline run details:

![build pipeline output status](img/040_build_pipeline_output_status.png)

You can click on it to see in details which files where published.

![build pipeline artifacts](img/050_build_pipeline_artifacts.png)

We will see in the next task how to work with these artifacts. Before we proceed, please take a note of the ID of our build pipeline:

![pipeline definition id](img/060_pipeline_definitionid.png)

We need this `definitionId` to reference to our build pipeline as part of our next task.

<!-- ------------------------------------------------------------------------------------------ -->
---

## Exercise 8.2: Working with Build Artifacts

In our previous task we have created a build pipeline that has copied a subset of files from a repository and published them as build artifacts.

We now want to consume these build artifacts to do something with them. Therefore we will now create a release pipeline.

1. Goto Pipelines > Pipelines
1. Click "New pipeline"
1. Select "Azure Repos Git (YAML)"
1. Select our repository
1. Select "Existing Azure Pipelines YAML file"
1. Select the correct branch (lab8)
1. Select `/.azdo/pipelines/release.pipeline.yml`
1. Click on "Continue"

    You will now see our example release pipeline:

    ![review release pipeline](img/070_review_release_pipeline.png)

    The pipeline contains three main areas.

    In 1) you see the variables definition. We are specifying here the buildPipelineDefinitionId that contains the ID of our build pipeline (created in the previous task).

    In 2) you see the `DownloadPipelineArtifact@2` task that is downloading our artifact that we have created in our build pipeline. There are more parameters to make this even more specific.

    In 3) you see how we execute a script that comes from our artifact.

1. Update the `buildPipelineDefinitionId` with the definitionId from our previous task.
1. Click on "Save and run" (twice)
1. In our job details, click on "Job"

Here we will now find the `Download Pipeline Artifacts` task that is downloading the artifacts from a specific build pipeline:

![review release output](img/080_review_release_pipeline_output.png)

And an example where we execute a script that is coming from our artifacts:

![review release output](img/090_review_release_pipeline_output2.png)

And that was a short introduction into CI and CD (build and release) with a YAML-based pipeline in Azure DevOps.

This separation can be useful in many ways.

* Single Build, multiple Release (for example with a shared scripts or template repository)
* Versioning Artifacts like Templates and Scripts to release a specific version of it

<!-- ------------------------------------------------------------------------------------------ -->
---

This completes Lab 8.

No Next Lab | [Previous Lab](../lab7/lab7.md) | [Table of Contents](/README.md)
