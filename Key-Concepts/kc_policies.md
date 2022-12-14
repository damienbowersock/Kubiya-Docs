---
layout: default
title: Policies
parent: Key Concepts
nav_order: 4
---
# What are Policies?

Kubiya uses a policy based approach to control access to the platform. This means that you can control who can access the platform, and what they can do once they are in the platform.

Kubiya policies are extensible. This means that you can add your own policies to the platform. You can also modify the existing policies to suit your needs.

Policies are defined using a simple YAML or JSON syntax. You can use the Kubiya CLI to manage policies in terms of creating, updating, and deleting policies.

In Kubiya, every action is enforced by a policy - which means that users cannot perform actions that are not allowed by an existing policy.

## Enforced Actions
The following actions are enforced by a policy:

* CLI commands
* API calls
* Web UI actions
* Integrations (e.g. Slack - opening a modal)

## Policy Types
Kubiya supports the following policy types:

* #### ABAC - Attribute Based Access Control. This policy type allows you to define policies based on attributes. For example, you can define a policy that allows users to access the platform only if they are part of a specific group.
* #### RBAC - Role Based Access Control. This policy type allows you to define policies based on roles. For example, you can define a policy that allows users to access the platform only if they have a specific role.


## Approval flows
In cases where a user needs to perform an action that is not allowed by a policy, Kubiya will ask the user to request approval from a user that is allowed to perform the action. Approval flows does not require any logic to be written. Instead, the approval flows are automatically generated by Kubiya based on the context of the action.

For example, if a user tries to create a new issue in JIRA, Kubiya will automatically generate an approval flow that will ask the user to request approval from a user that is allowed to create issues in JIRA.