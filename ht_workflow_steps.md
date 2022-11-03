---
layout: default
title: Workflow Steps
parent: Workflows
grand_parent: How To Guides
nav_order: 2
---
# Workflow Steps

Workflows are comprised of steps.  Steps allow for interaction with the user, such as gathering input or asking for confirmation, as well as interaction with outside services such as AWS, Jira, etc.  Steps that interact with outside services are defined by Actions and are collected in Action Stores that can be imported into Kubiya and called from your workflow.

## Defining a Step

As we saw when building [My First Workflow](ht_first_workflow.html), steps are defined in a YAML file that outlines the workflow.  Each step must have at least an ID and a Type.

### Step ID

```yaml
steps:
  - id: <step ID>
```

The Step ID gives the step a name.  This name can be used to direct the workflow to execute the step and also names any variables that may be defined during the workflow.

### Step Type

```yaml
steps:
  - id: <step ID>
    type: <type>
```

The Step Type defines the type of activity the step will take.  Valid Step Types are:
    1. Input - Requesting a single input from the user.
    2. Multi-Input - Requesting the user select from several options.
    3. Message - Providing output to the user
    4. Action - Interacting with an external system via an Action
    5. Condition - Make a decision based on an if/then criteria
    6. Exit - Exit the workflow

For a detailed explanation of Step Types and how to define them, please refer to the syntax guide.

### Step Prompt

```yaml
steps:
  - id: <step ID>
    type: <type>
    prompt: "<your text string>"
```

Step prompts instructs Kubiya to send some output to user.  This may be asking a question, giving an instruction, etc.  Prompts can include variables as we saw in the example workflow:

```yaml
  prompt: Hello, ${name}.  Welcome to Kubiya!
```



