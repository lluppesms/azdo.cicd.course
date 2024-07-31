# Activate CICD with Azure DevOps Using YML and Bicep

![hero](img/hero.png)

In this workshop, you will learn how to use Azure DevOps to automate common tasks like building, testing, and deploying your code. You will learn how to create a pipeline using YML and Bicep, and how to use triggers, variables, and templates to make your pipeline more flexible and reusable. You will also learn how to deploy your code to multiple environments and how to create a library of reusable templates.

We'll start from scratch and build up to a full CI/CD YML pipeline that builds, tests, and deploys a simple web application to Azure. By the end of this workshop, you will have a solid understanding of how to use Azure DevOps to automate your development process and how to create a reusable pipeline components that can be easily adapted to different projects and environments.

## Getting Started

You will need an Azure DevOps Organization and Project in order to complete this workshop. If you don't already have an Azure DevOps Organization, you can create one for free at [dev.azure.com](http://dev.azure.com). You will also need an Azure Subscription to deploy resources to Azure.  For more detailed information on setting an organization and project, see the [Create an Azure DevOps Project](/Labs/lab0/Create-Azdo-Project.md) document for more information.

Once we proceed to the Bicep part of the course, you will also want an editor like VS Code to edit the YML and Bicep files, and a few key extensions to make things better. See the [Visual Studio Code Setup](/Labs/lab0/Visual-Studio-Code.md) document for more information.

If you need a Build Agent for this class, you can refer to the [Creating a Custom Build Agent](/Labs/Build-Agents/desktop-runner/README.md) document to assist you in creating it. You can use the default of the Microsoft Hosted Agents, but if you have a large class it may be better to each have your own custom custom agent.

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
  <summary>Before You Start...</summary>

* [Lab 0.1 - Create an Azure DevOps Project](/Labs/lab0/Create-Azdo-Project.md)
* [Lab 0.2 - Create a Custom Build Agent](/Labs/Build-Agents/desktop-runner/README.md)
* [Lab 0.3 - Set up Visual Studio Code (Optional)](/Labs/lab0/Visual-Studio-Code.md)

</details>

<details>
  <summary>Lab 1 - Introduction To Pipelines</summary>

* [Lab 1 - Introduction](/Labs/lab1/lab1.md)
  * [Create a YAML-Pipeline via GUI](/Labs/lab1/lab1.md#exercise-11-create-a-yaml-pipeline-via-gui)
  * [Run your pipeline](/Labs/lab1/lab1.md#exercise-12-run-your-pipeline)
  * [Analyze the output](/Labs/lab1/lab1.md#exercise-13-analyze-the-output)
  * [Use the assistant to add tasks](/Labs/lab1/lab1.md#exercise-14-use-the-assistant-to-add-tasks)
  * [Extend the pipeline with variables](/Labs/lab1/lab1.md#exercise-15-extend-your-pipeline-with-variables)
  * [Check the pipeline within the repository](/Labs/lab1/lab1.md#exercise-16-check-the-pipeline-within-your-repository)

</details>

<details>
  <summary>Lab 2 - Tasks, Jobs, Stages and Dependencies</summary>
  
* [Lab 2 - Tasks, Jobs, Stages and Dependencies](/Labs/lab2/lab2.md)
  * [Separating tasks into different jobs](/Labs/lab2/lab2.md#exercise-21-separating-tasks-into-different-jobs)
  * [Adding dependencies between jobs](/Labs/lab2/lab2.md#exercise-22-adding-dependencies-between-jobs)
  * [Splitting our pipeline into stages](/Labs/lab2/lab2.md#exercise-23-splitting-our-pipeline-into-stages)
  * [Dependencies between stages](/Labs/lab2/lab2.md#exercise-24-adding-dependencies-between-jobs-and-stages)
  * [Approvals](/Labs/lab2/lab2.md#exercise-25-approvals)

</details>

<details>
  <summary>Lab 3 - Working with Templates</summary>

* [Lab 3 - Working with Templates](labs/lab3/lab3.md)
  * [Load steps from templates](/Labs/lab3/lab3.md#exercise-31-load-steps-from-templates)
  * [Reusing stages with templates](/Labs/lab3/lab3.md#exercise-32-reusing-stages-with-templates)
  * [Conditional Execution](/Labs/lab3/lab3.md#exercise-33-conditions)
  * [Skipping stages](labs/lab3/lab3.md#exercise-34-skipping-stages)

</details>

<details>
  <summary>Lab 4 - Triggers</summary>
  
* [Lab 4 - Triggers](/Labs/lab4/lab4.md)
  * [Working with triggers and branches](/Labs/lab4/lab4.md#exercise-4-1-working-with-triggers-and-branches)
  * [Working with triggers and paths](/Labs/lab4/lab4.md#exercise-42-working-with-triggers-and-path)
  * [Schedule Triggers](labs/lab4/lab4.md#exercise-43-scheduled-trigger)
  * [Pull Request Triggers](labs/lab4/lab4.md#exercise-44-pull-request-triggers)

</details>

<details>
  <summary>Lab 5 - More Variables and Parameters</summary>

* [Lab 5 - More Variables and Parameters](/Labs/lab5/lab5.md)
  * [5.1 Using Parameters](/Labs/lab5/lab5.md#exercise-51-using-parameters)
  * [5.2 Using Local Variables](/Labs/lab5/lab5.md#exercise-52-local-variables)
  * [5.3 Variable Template Files](/Labs/lab5/lab5.md#exercise-53-variable-template-files)
  * [5.4 Predefined Variables](/Labs/lab5/lab5.md#exercise-54-predefined-variables)
  * [5.5 Creating Variables in Code](/Labs/lab5/lab5.md#exercise-55-creating-variables-in-code)
  * [5.6 Using Variable Groups](/Labs/lab5/lab5.md#exercise-56-using-variable-groups)
  * [5.7 Loading Values from Key Vault](/Labs/lab5/lab5.md#exercise-57-loading-values-from-key-vault)
  * [5.8 Verbose Logs](/Labs/lab5/lab5.md#exercise-58-verbose-logs)

</details>

<details>
  <summary>Lab 6 - Multiple Environments and Stages</summary>

* [Lab 6 - Multiple Environments and Stages](/Labs/lab6/lab6.md)
  * [6.1 Creating AzDO Environments](/Labs/lab6/lab6.md#exercise-61-creating-azdo-environments)
  * [6.2 Deploying to Multiple Environments with Dependencies](/Labs/lab6/lab6.md#exercise-62-deploying-to-multiple-environments-with-dependencies)

</details>

<details>
  <summary>Lab 7 - Reusable Libraries</summary>

* [Lab 7 - Reusable Libraries](/Labs/lab7/lab7.md)
  * [7.1 Creating a Template Repository](/Labs/lab7/lab7.md#exercise-71-creating-a-template-repository)

</details>

<details>
  <summary>Lab 8 - Splitting CI and CD</summary>

* [Lab 8 - Splitting CI and CD](/Labs/lab8/lab8.md)
  * [Creating a Build pipeline and saving the artifacts](labs/lab8/lab8.md#exercise-81-build-pipelines-and-artifacts)
  * [Creating a Release Pipeline using a pre-built artifact](labs/lab8/lab8.md#exercise-82-working-with-build-artifacts)

</details>

## Origins

This workshop is loosely based on [a lab](https://github.com/heoelri/adopac) that was initially created by `Rathish Ravikumar` and `Heyko Oelrichs` of Microsoft for an internal training event, and was then updated by `Lyle Luppes` to add more modules and content.
