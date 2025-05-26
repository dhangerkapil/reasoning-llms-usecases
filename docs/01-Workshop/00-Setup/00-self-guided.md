# Lab 1: Setup AI Project

!!! quote "BY THE END OF THIS LAB YOU SHOULD HAVE"

    1. Set your tab preference (Microsoft Build Attendee vs. Self-Guided Learner)
    1. A pre-configured development environment in GitHub Codespaces
    1. An provsisoned Azure AI project in Azure AI Foundr

---

## 1. Before You Begin

This lab is setup for use by both in-venue attendees (75-minute session) and at-home learners (self-paced). The setup instructions differ based on this context. **Pick the path that fits your current learning context** - this is automatically enforced site-wide.


=== "Microsoft Build Attendee"

    !!! info "I am currently a Lab 333 attendee **AT MICROSOFT BUILD 2025** (75 minutes)"

=== "Self-Guided Learner"

    !!! quote "I am working through the lab **AT HOME** with my Azure subscription (self-paced)"

---

## 1. Local Environment

You are currently using a _prebuild_ version of this repository on GitHub Codespaces. This development environment is preconfigured with all the tools you need to complete the lab. Let's use these tools to configure the local environment to work with Azure, next!

---

## 2. Azure Infrastructure

In this step, we'll connect our local development environment (GitHub Codespaces) to a provisioned Azure AI Foundry project.


=== "Microsoft Build Attendee"

    !!! info "You will be using the pre-provisioned Skillable Azure Credentials in this section"

    1. Visit the Skillable VM tab in your browser - verify you see Azure credentials
    1. Return to the Codespaces tab - open the VS Code terminal and run this command

        ``` title="" linenums="0"
        az login --use-device-code
        ```
    1. This starts a browser-based authentication flow. Follow the instructions in the terminal to complete this process. **When logging into Azure, use the Skillable credentials above.**
    1. Return to the VS Code terminal when done and press `Enter` if asked about subscription choice. _Congratulations! You are logged into Azure!_.

    You don't need to deploy any infrastructure - **this is already done for you!**

=== "Self-Guided Learner"

    !!! quote "You will need to use your personal Azure Subscription for this step"

    1. Open the VS Code terminal and run this command

        ``` title="" linenums="0"
        az login --use-device-code
        ```
    1. This starts a browser-based authentication flow. Follow the instructions in the terminal to complete this process. *When prompted to log in, use your own Azure credentials.*
    1. Return to the VS Code terminal when done. 
    1. Select the subscription of your choice, or press `Enter` for the default that is offered. *You are logged into Azure!*
    1. Next, run this command.  *You created a resource group called Lab333 in region EastUS 2*
        ``` title="" linenums="0"
        az group create --name Lab333 --location 'EastUS 2'
        ```
    1. Wait till that completes. *Your resource group is now ready to be provisioned*.

        ``` title="" linenums="0"
        {
            "id": "/subscriptions/XXXXXX/resourceGroups/Lab333",
            "location": "eastus2",
            "managedBy": null,
            "name": "Lab333",
            "properties": {
                "provisioningState": "Succeeded"
            },
            "tags": null,
            "type": "Microsoft.Resources/resourceGroups"
        }
        ```

    1. Run this command to deploy resources to that resource group. _This takes a few minutes_.

        ``` title="" linenums="0"
        az deployment group create --name reasoning-template --resource-group Lab333 --template-file infra/template.json
        ```

    1. You will be prompted for a **uniqueSuffix** - provide a random 4-digit number. _This will reduce naming conflicts with soft-deleted resources from previous runs, that aren't yet purged._

    1. The process takes a few minutes to complete. **Congratulations! Your infra is ready!**
