---
layout: default
title: Knowledge
parent: How To Guides
has_children: true
nav_order: 3
---
# Teaching Kubiya to be Smarter

## Knowledge Overview

Kubiya Knowledge is a powerful tool that allows the user to interact with Kubiya using natural language.  This could be as simple as creating "shortcuts" for users to launch workflows.  Kubiya's Knowledge capabilities are intelligent enough to automatically correct for typos and use fuzzy logic to "guess" what a user was trying to do.  This dramatically decreases the friction users may experience when engaging with Kubiya.

## Example Usage

To teach Kubiya something new, we can leverage the Pinned message menu in the Slack App.  Click the 'Knowledge' button in the pinned message as below.

![](../images/know-pinned.png)

This launches an internal workflow that will first ask you if you want to add a new Knowledge entry or delete an existing entry.  Click the 'Add' button.

![](../images/know-add.png)

Adding a new entry requires Slack to launch a form dialog, click the "Fill Form" button.

![](../images/know-fillform.png)

When completing the form, the first field will be the name of the Knowledge Topic you are creating.  This will be used if you want to delete this entry in the future.

The next two fields are example natural language statements that the system will react to when a user issues them.  In our example we used 'gather user info' and 'collect user data'.

![](../images/know-form.png)

Once you teach Kubiya what natural language statements to respond to, you will be asked what Kubiya should do when they are invoked.  You may choose to launch a workflow or reply to the user with a text message.  Select "Run a Workflow".

![](../images/know-workflow.png)

Select which workflow you would like to invoke.

![](../images/know-select.png)

That's it!

![](../images/know-done.png)

## Testing Knowledge

To test your newly trained knowledge, simple issue the natural language command that you trained.



