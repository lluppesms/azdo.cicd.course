# Creating Custom Build Agents

If you need additional build agents, you can purchase additional Microsoft Hosted Agents in your Azure DevOps Organization Settings -> Billing.  That is the easiest way to do this, but there is an additional charge for these. You can create your own custom build agents.

This lab will walk you through the process of creating your own custom Azure Devops Build Runners. You can create them in one of two ways, depending on your use case:

* [Use Azure Container Apps as the build agent](./aca-runner/README.md)
* [Use your own desktop as the build agent](./desktop-runner/README.md)

The Desktop version would also apply if you want to use a VM in Azure (or on-prem) as the build agent.

## References

[Tutorial: Deploy self-hosted CI/CD runners and agents with Azure Container Apps jobs](https://learn.microsoft.com/en-us/azure/container-apps/tutorial-ci-cd-runners-jobs?tabs=bash&pivots=container-apps-jobs-self-hosted-ci-cd-azure-pipelines)

[Self-hosted Windows agents](https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/windows-agent?view=azure-devops)
