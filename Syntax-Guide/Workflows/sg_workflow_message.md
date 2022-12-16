---
layout: default
title: Message Steps
parent: Workflow Syntax
grand_parent: Syntax Guide
nav_order: 5
---

# Workflow Message Step Syntax Guide

Message Steps allow Kubiya to provide output back to the user and are one of the simplest of all step types.  Message steps consist of an 'id:' key, a 'type:' key and a 'prompt:' key as follows:

```yaml
id: <message step name>
type: message
prompt: <output to be sent to user>
```

Common use cases for message prompts are to provide status updates on actions that may have occured, log error messages, etc.
## prompt: Keys

The Prompt is a single string of characters that can be sent as output to the user interface.  The format for prompts follow normal string formatting conventions.

### New Lines

If you would like to break your output into separate lines of text, you may use the '\n' character to begin a new line of text.  As an example:

```yaml
id: example_output
type: message
prompt: "This is line 1 of text. \nThis is line 2 of text."
```
Output:

    This is line 1 of text.
    This is line 2 of text.

### Variables

Using variables in the output allows the administrator to provide context to the user regarding the actions that may have been taken.  As an example, consider that a previous step launched an EC2 instance on AWS named "Database-Server".  This name was captured in a variable as {InstanceName}.  We may want to let the user know that the instance was successfully launched as follows:

```yaml
id: launch_success
type: message
prompt: "AWS EC2 Instance ${InstanceName} was successfully launched."
```

This would result in the following output:

    AWS EC2 Instance Database-Server was successfully launched.

### Hyperlinks

Should you wish to provide the user a hyperlink to click, this can be done by separating the reference in '< >'.  Within the angle brackets, use the format of "<link|clickable text>" as follows:

```yaml
<https://eu-west1.console.aws.amazon.com/ec2/v2/home | View EC2 Home Page>
```

Additionally using variable will allow the administrator to provide a link directly to specific resources.  As in our previous example, we could provide a link to our new "Database-Server" instance with a link similar to:

```yaml
<https://eu-west1.console.aws.amazon.com/ec2/v2/home?region=eu-west-1#InstanceDetails:instanceId=${InstanceName}|View on AWS Console>
```

This would result in the link https://eu-west1.console.aws.amazon.com/ec2/v2/home?region=eu-west-1#InstanceDetails:instanceId=Database-Server being linked to the text "View on AWS Console"

