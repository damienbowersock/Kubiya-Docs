---
layout: default
title: Action Steps
parent: Workflow Syntax
grand_parent: Syntax Guide
nav_order: 1
---

# Workflow Action Steps

## Defining an Action Step

```yaml
    - id: <name of step>
      type: action
      action:
        store: <name of action store that defines the action>
        name: <name of action to take>
        parameters: {}
```

### action: Definitions

#### store:
This allows the workflow creator to select a set of actions from a specific action store.
Example:
```yaml
    action:
        store: aws
```
This selects the 'aws' action store that defines commands to allow for interacting with AWS environments

---
#### name:
This allows the workflow creator to select the specific action, from within the store, to use.
Example:
```yaml
    action:
        store: aws
        name: "ecs.ListClusters"
```
This requests the list of Elastic Container Service Clusters from AWS.

---
#### parameters:
This allows the workflow creator to pass any needed parameters into the command stream.
Example:
```yaml
    action:
        store: aws
        name: "ecs.ListServices"
        parameters:
            cluster: {<name of cluster>}
```
This example passes the name of a cluster to the ECS List Services command.  The return would be a list of services that the given cluster uses.

If no parameters are necessary, simply pass an empty set of braces as:
```yaml
        parameters: {}
```

