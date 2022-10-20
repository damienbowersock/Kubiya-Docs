---
layout: default
title: Workflows
parent: Key Concepts
nav_order: 1
---
# What are Workflows?

Workflows are a way to describe a sequence of actions that can be executed by Kubiya.

Workflows are defined using the [YAML](https://yaml.org) format and are based on the Kubiya domain specific language (DSL).

The Kubiya DSL is a simple and intuitive way to define workflows through a combination of Triggers and Steps.

## Triggers
Triggers are the starting point of a workflow and represent an event that invokes a series of actions.

Kubiya supports a variety of triggers:

* ### Interaction Triggers
    Interaction triggers are invoked when a user interacts with a user in a pre-described way.  Kubiya understands several interaction triggers. For example:

    * Natural Language - simple English sentences that are used to trigger a workflow
    * Slash Commands - slash commands that are used to trigger a workflow (e.g. /hello)
    * Interactive Components - interactive components that are used to trigger a workflow (e.g. buttons, menus, etc.)

* ### Event Triggers
    Event triggers are used to define when a workflow should be executed based on an event that occurs in an integrated system. Kubiya supports a variety of events sources using the CloudEvents standard. For example:

    * Slack Events - Slack events that are used to trigger a workflow (e.g. message.im)
    * GitHub Events - GitHub events that are used to trigger a workflow (e.g. pull_request)
    * AWS Events - AWS events that are used to trigger a workflow (e.g. ec2:RunInstances)

* ### Time (Cron) Triggers
    Time triggers are used to define when a workflow should be executed based on a time schedule. Schedules are simple cron expressions that are used to trigger a workflow (e.g. 0 0 * * *).

## Steps
The series of actions that occur when a workflow is triggered are known as steps. Each step is a single action, performed by Kubiya sequentially, as prescribed by the workflow definition.

Kubiya can perform many types of steps allowing for complex workflows.  Types of steps include:

* ### Input Steps
Input steps are used to define a step that is used to get input from the user. (e.g. text, number, etc.)

* ### Action Steps
Action steps are used to define a step that is used to execute an action. (such as opening a GitHub Pull request, or causing an AWS Lambda function to be executed)

* ### Condition Steps
Condition steps are used to define a condition that is used to determine the next step in the workflow based on the result of the condition.

* ### JQ Steps
JQ steps are used to define a step that is used to transform the workflow context using the JQ language.  Details for using JQ can be found [here](https://stedolan.github.io/jq/).

* ### Wait Steps
Wait steps are used to define a step that is used to wait for a specified amount of time, or until a condition is met. (such as waiting for a GitHub Pull request to be merged)


## Importing Workflows
Many times an operator may wish to reuse a workflow created by another operator or third-party.  Kubiya allows you to import pre-defined workflows from several sources:

* Using the Kubiya UI drag and drop editor
* SVN - such as GitHub, GitLab, Bitbucket
* From a local directory - such as your computer


⏭️ Next: [Actions](kc_actions.html)