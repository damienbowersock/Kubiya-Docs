---
layout: default
title: Workflow Syntax
nav_order: 1
parent: Syntax Guide
has_children: true
---
# Workflow Syntax

## Workflow CLI Commands

### Validate a Workflow

Validating a workflow confirms that the workflow meets the syntax and error standards set forth by Kubiya.

```bash
kubiya workflow validate <filename>
```

### Upload a Workflow

To upload a workflow to the Kubiya SaaS platform use the following command.  Note: a workflow should pass validation prior to being uploaded.

```bash
kubiya workflow upload <workflow_filename>
```

### Listing all Workflows

Listing the workflows will show which workflows have been sucessfully uploaded for use.

```bash
kubiya workflow list
```

### Describing a Workflow

Desicribing a workflow displays the construction of the workflow by summarizing the following:
- Workflow Type (i.e. conversation)
- Names of each step.
- Any Actions used
- Conditional tests that define the logic
- A list of steps that allow for input
- Any variables used (tokens)

```bash
kubiya workflow describe <workflow_name>
```

### Launch a Worflow from the CLI

Kubiya can launch a workflow from the CLI to be run in Slack.  By default the workflow will be launched for the user authenticated to the CLI.  If preferred, the workflow can be launched for a different user with the '-u' flag.

```bash
kubiya workflow launch -n <workflow_name> -u <user_email_optional>
```





