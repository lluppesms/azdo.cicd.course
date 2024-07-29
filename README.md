# Activate CICD with Azure DevOps Using YML and Bicep

![hero](img/hero.png)

In this workshop, you will learn how to use Azure DevOps to automate common tasks like building, testing, and deploying your code. You will learn how to create a pipeline using YML and Bicep, and how to use triggers, variables, and templates to make your pipeline more flexible and reusable. You will also learn how to deploy your code to multiple environments and how to create a library of reusable templates.

We'll start from scratch and build up to a full CI/CD YML pipeline that builds, tests, and deploys a simple web application to Azure. By the end of this workshop, you will have a solid understanding of how to use Azure DevOps to automate your development process and how to create a reusable pipeline components that can be easily adapted to different projects and environments.

## Getting Started

You will need an Azure DevOps Organization and Project in order to complete this workshop. If you don't already have an Azure DevOps Organization, you can create one for free at [dev.azure.com](http://dev.azure.com). You will also need an Azure Subscription to deploy resources to Azure.  For more detailed information on setting an organization and project, see the [Before You Start](/Labs/lab0/before-you-start.md) document for more information.

Once we proceed to the Bicep part of the course, you will also want an editor like VS Code to edit the YML and Bicep files, and a few key extensions to make things better. See the [Visual Studio Code Setup](/Labs/lab0/Visual-Studio-Code.md) document for more information.

If you need additional Build Agents for this class, you can refer to the [Creating Custom Build Agents](/Labs/Build-Agents/README.md) document to assist you in creating them.

## Labs

This workshop will cover a series of labs, in which you will learn to create effective YML pipelines.

<!-- 
* [Lab 1 - Introduction](/Labs/lab1/lab1.md)
* [Lab 2 - Tasks, Jobs, Stages and Dependencies](/Labs/lab2/lab2.md)
* [Lab 3 - Working with Templates](labs/lab3/lab3.md)
* [Lab 4 - Triggers](/Labs/lab4/lab4.md)
* [Lab 5 - More About Variables and Parameters](/Labs/lab5/lab5.md)
* [Lab 6 - Using Multiple Environments and Stages](/Labs/lab6/lab6.md)
* [Lab 7 - Creating Reusable Libraries](/Labs/lab7/lab7.md)
* [Lab 8 - Splitting CI and CD](/Labs/lab8/lab8.md)
-->

<details>
  <summary>Before you start</summary>

* [Lab 0 - Before you start](/Labs/lab0/before-you-start.md)

</details>

<details>
  <summary>Lab 1 - Introduction To Pipelines</summary>

* [Lab 1 - Introduction](/Labs/lab1/lab1.md)
  * [Create a YAML-Pipeline via GUI](/Labs/lab1/lab1.md#11-create-a-yaml-pipeline-via-gui)
  * [Run your pipeline](/Labs/lab1/lab1.md#12-run-your-pipeline)
  * [Analyze the output](/Labs/lab1/lab1.md#13-analyze-the-output)
  * [Use the assistant to add tasks](/Labs/lab1/lab1.md#14-use-the-assistant-to-add-tasks)
  * [Extend the pipeline with variables](/Labs/lab1/lab1.md#15-extend-your-pipeline-with-variables)
  * [Check the pipeline within the repository](/Labs/lab1/lab1.md#16-check-the-pipeline-within-your-repository)

</details>

<details>
  <summary>Lab 2 - Tasks, Jobs, Stages and Dependencies</summary>
  
* [Lab 2 - Tasks, Jobs, Stages and Dependencies](/Labs/lab2/lab2.md)
  * [Separating Tasks into different Jobs](/Labs/lab2/lab2.md#21-separating-tasks-into-different-jobs)
  * [Adding dependencies between Jobs](/Labs/lab2/lab2.md#22-adding-dependencies-between-jobs)
  * [Splitting our pipeline into Stages](/Labs/lab2/lab2.md#23-splitting-our-pipeline-into-stages)
  * [Dependencies between Stages](/Labs/lab2/lab2.md#24-adding-dependencies-between-jobs-and-stages)
  * [Approvals](/Labs/lab2/lab2.md#25-approvals)

</details>

<details>
  <summary>Lab 3 - Working with Templates</summary>

* [Lab 3 - Working with Templates](labs/lab3/lab3.md)
  * [Load steps from templates](/Labs/lab3/lab3.md#31-load-steps-from-templates)
  * [Reusing stages with templates](/Labs/lab3/lab3.md#32-reusing-stages-with-templates)
  * [Conditions](/Labs/lab3/lab3.md#33-conditions)
  * [Skipping stages](labs/lab3/lab3.md#34-skipping-stages)

</details>

<details>
  <summary>Lab 4 - Triggers</summary>
  
* [Lab 4 - Triggers](/Labs/lab4/lab4.md)
  * [Working with triggers and branches](/Labs/lab4/lab4.md#4-1-working-with-triggers-and-branches)
  * [Working with triggers and path](/Labs/lab4/lab4.md#42-working-with-triggers-and-path)
  * [Scheduled Triggers](labs/lab4/lab4.md#43-scheduled-trigger)
  * [Scheduled Triggers](labs/lab4/lab4.md#44-pull-request-triggers)

</details>

<details>
  <summary>Lab 5 - More Variables and Parameters</summary>

* [Lab 5 - More Variables and Parameters](/Labs/lab5/lab5.md)
  * [5.1 Using Parameters](/Labs/lab5/#51-using-parameters)
  * [5.2 Local Variables](/Labs/lab5/#52-local-variables)
  * [5.3 Variable Template Files](/Labs/lab5/#53-variable-template-files)
  * [5.4 Predefined Variables](/Labs/lab5/#54-predefined-variables)
  * [5.5 Creating Variables in Code](/Labs/lab5/#55-creating-variables-in-code)
  * [5.6 Using Variable Groups](/Labs/lab5/#56-using-variable-groups)
  * [5.7 Loading Values from Key Vault](/Labs/lab5/#57-loading-values-from-key-vault)
  * [5.8 Verbose Logs](/Labs/lab5/#58-verbose-logs)

</details>

<details>
  <summary>Lab 6 - Multiple Environments and Stages</summary>

* [Lab 6 - Multiple Environments and Stages](/Labs/lab6/lab6.md)
  * [6.1 Creating AzDO Environments](/Labs/lab6/#61-creating-azdo-environments)
  * [6.2 Deploying to Multiple Environments with Dependencies](/Labs/lab6/#62-deploying-to-multiple-environments-with-dependencies)

</details>

<details>
  <summary>Lab 7 - Reusable Libraries</summary>

* [Lab 7 - Reusable Libraries](/Labs/lab7/lab7.md)
  * [7.1 Creating a Template Repository](/Labs/lab7/#71-creating-a-template-repository)

</details>

<details>
  <summary>Lab 8 - Splitting CI and CD</summary>

* [Lab 8 - Splitting CI and CD](/Labs/lab8/lab8.md)
  * [Build pipelines and artifacts](labs/lab8/lab8.md#81-build-pipelines-and-artifacts)
  * [Working with build artifacts](labs/lab8/lab8.md#82-working-with-build-artifacts)

</details>

## Origins

This workshop is loosely based on [https://github.com/heoelri/adopac](a repository) that was initially created by `Rathish Ravikumar <rathishr@microsoft.com>` and `Heyko Oelrichs <heoelri@microsoft.com>` for an internal training and was then updated by `Lyle Luppes <lyleluppes@microsoft.com>` to add more modules and content.
