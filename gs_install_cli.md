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

<a href="https://kubiya-cli.s3.eu-west-1.amazonaws.com/versions/0.8.0/mac/intel/kubiya-cli">Mac OSX - Intel</a> 

<a href="https://kubiya-cli.s3.eu-west-1.amazonaws.com/versions/0.8.0/mac/apple/kubiya-cli">Mac OSX - Apple</a> 

<a href="https://kubiya-cli.s3.eu-west-1.amazonaws.com/versions/0.8.0/linux/amd64/kubiya-cli"> Linux (amd64) </a> 

<a href="https://kubiya-cli.s3.eu-west-1.amazonaws.com/versions/0.8.0/linux/arm64/kubiya-cli">Linux (arm64)</a>

Copy the CLI to a location in your PATH and make it executable.

Do so by running the following commands:

    ```bash
        sudo cp kubiya /usr/local/bin
        sudo chmod +x /usr/local/bin/kubiya
    ```

Check that the newly installed Kubiya CLI is working by running the following command:

    ```bash
        kubiya --version
    ```

The CLI will output the following if the installation was successful:

    Version 1.0.0 (git hash: ae8f8f)

(Note: the version number can change as well as the git hash based on the version of the CLI)

⏭️ Next: [Authenticate using the CLI](gs_authenticae.html)

