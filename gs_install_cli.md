---
layout: default
title: Installing the Kubiya CLI
parent: Getting Started
nav_order: 1
---
# Installing the Kubiya CLI

The Kubiya CLI is a simple command line interface which allows you to interact with Kubiya from the command line. You can use the CLI to:

* Add Integrations
* Manage Workflows
* Manage Access Policies

## Installation
The Kubiya CLI is available for multiple platforms. You can download the CLI using the following links:

<button onclick="example.com">Mac OSX - Intel</button> <button onclick="example.com">silicon Mac OSX - Apple silicon</button> <button onclick="example.com"> Linux (amd64) </button> <button onclick="example.com">Linux (arm64)</button>

Copy the CLI to a location in your PATH and make it executable.

Do so by running the following commands:

    sudo cp kubiya /usr/local/bin
    sudo chmod +x /usr/local/bin/kubiya

Check that the newly installed Kubiya CLI is working by running the following command:

    kubiya --version

The CLI will output the following if the installation was successful:

    Version 1.0.0 (git hash: ae8f8f)

(Note: the version number can change as well as the git hash based on the version of the CLI)

⏭️ Next: [Authenticate using the CLI](Authenticating_Kubiya_from_the_CLI)

