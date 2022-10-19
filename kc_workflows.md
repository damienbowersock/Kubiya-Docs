---
layout: default
title: Workflows
parent: Key Concepts
nav_order: 1
---
# What are Workflows?

Workflows are a way to describe a sequence of actions that can be executed by Kubiya.

Workflows are defined using the [YAML](https://yaml.org) format and are based on the Kubiya domain specific language (DSL).

The Kubiya DSL is a simple and intuitive way to define workflows. It is based on a set of core concepts which are explained in the next sections.

Kubiya supports importing workflows from a variety of sources.

* Using the Kubiya UI drag and drop editor
* SVN - such as GitHub, GitLab, Bitbucket
*From a local directory - such as your computer

## Workflow DSL
The Kubiya DSL allows you to define workflows using a simple and intuitive syntax.

The DSL involves a combination of the core concepts which are explained in the next sections.

## Triggers
Triggers are the starting point of a workflow. They are used to define when a workflow should be executed.

Kubiya supports a variety of triggers:

### Interaction Triggers
Interaction triggers are used to define when a workflow should be executed based on a user interaction. Kubiya supports a variety of interaction triggers. For example:

* Natural Language - simple English sentences that are used to trigger a workflow
* Slash Commands - slash commands that are used to trigger a workflow (e.g. /hello)
* Interactive Components - interactive components that are used to trigger a workflow (e.g. buttons, menus, etc.)

### Event Triggers
Event triggers are used to define when a workflow should be executed based on an event. Kubiya supports a variety of events sources using the CloudEvents standard. For example:

* Slack Events - Slack events that are used to trigger a workflow (e.g. message.im)
* GitHub Events - GitHub events that are used to trigger a workflow (e.g. pull_request)
* AWS Events - AWS events that are used to trigger a workflow (e.g. ec2:RunInstances)

### Time (Cron) Triggers
Time triggers are used to define when a workflow should be executed based on a time schedule. Schedules are simple cron expressions that are used to trigger a workflow (e.g. 0 0 * * *).

## Steps
A workflow is a sequence of steps. Each step is a single action that is executed by Kubiya. In Kubiya, steps are based on types. Each type has a set of properties that are used to define the step.

Kubiya supports a variety of step types:

* Input Steps
* Input steps are used to define a step that is used to get input from the user. (e.g. text, number, etc.)

### Action Steps
Action steps are used to define a step that is used to execute an action. (such as opening a GitHub Pull request, or causing an AWS Lambda function to be executed)

### Condition Steps
Condition steps are used to define a condition that is used to determine the next step in the workflow based on the result of the condition.

### JQ Steps
JQ steps are used to define a step that is used to transform the workflow context using the JQ language.  Details for using JQ can be found [here](https://stedolan.github.io/jq/)

### Wait Steps
Wait steps are used to define a step that is used to wait for a specified amount of time, or until a condition is met. (such as waiting for a GitHub Pull request to be merged)

Next: Actions