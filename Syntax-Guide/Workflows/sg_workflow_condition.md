---
layout: default
title: Conditional Steps
parent: Workflow Syntax
grand_parent: Syntax Guide
nav_order: 4
---

# Workflow Conditional Step Syntax Guide

Conditional Steps in a workflow allow the author to implement basic logic.  These steps function as traditional If/Then/Else gates and can be used to make decisions based on the value of different variables during the workflow.  Based on these decisions an author could set values on new variables or jump to a specific step.

## Step Structure

All Conditional Steps start with a foundational structure as follows:

```yaml
id: <Step Name>
type: condition
if:
    arg: <Decision Argument>
    is: equals
    arg2: <Decision Argument 2
    then: <What to do if condition is true>
    else: <What to do if condition is false>
```

### if: 
This mapping defines the conditional step to use the If/Then/Else structure to determine which action to take.

### arg: and arg2:
This mapping defines which variables Kubiya will compare.

### is:
This mapping determines the evaluation criteria  Currently Kubiya only supports "equals" comparisons.  Thus, if <arg> equals <arg2>, the 'then:' statement will be executed.  Otherwise, the 'else:' statement will be executed.

### then: and else:
These mappings define what will occur if the conditions evaluate to True or False.  It should be noted that these mappings instruct Kubiya to execute a particular step that is named in the mapping.  This is similar to a GOTO statement in a Basic program.

## 

## Example
Let's consider a simple decision of whether the user wishes to exit the workflow or not, prior to the workflow's natural completion.  The first thing we should do is ask the user if they wish to exit.  We can do that using an [input step](../sg_workflow_input.html) as follows:

```yaml
id: terminate
type: input
prompt: "Would you like to exit the workflow?"
value_type: boolean
```

This will prompt the user to to answer the yes/no question of "Would you like to exit the workflow?"  The user's answer will be stored in a variable named for the step: {terminate}.  We can then use this to create a conditional exit decision as follows:

```yaml
id: conditional_exit
    type: condition
    if:
      arg: ${terminate}
      is: equals
      arg2: "true"
      then: exit
      else: <do something else>
```

Since the conditional step instruct Kubiya to jump to a particular step, in this case 'exit', we need to define the step that will be executed as follows:

```yaml
id: exit
type: exit
```





