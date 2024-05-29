# AWS Access Keys, CLI, and SDK

There are three options for accessing AWS.

* AWS Management Console
* CLI - Protected by access keys
* AWS SDK - for code. Protected by access keys

Access keys are generated through the AWS Console.

Users are responsible for their own access keys.

There is both an access key and a secret access key. 

## The AWS CLI

A tool that allows you to use your terminal to give commands to AWS. Direct access to the public APIs of AWS services.

A good alternative to the AWS console, which many professionals don't use at all.

## The AWS SDK

This isn't for user access, its for programmatic access. The SDK supports many languages. There is also a mobile SDK. 

The CLI itself is built on the SDK for Python.

## AWS CLI Setup on MacOS

* You want to install version 2. Just Google for a link.
* There are multiple ways to install the CLI tools. The command line method is trivially easy, just a cut and paste into the terminal. The GUI installed also looks very easy.

## Creating Access Keys

Go to User => Security Credentials => Create Access Key

## Cloudshell

Cloudshell is a browser-based terminal but it isn't available in all regions. It's basically a remote Linux terminal and it has some nice features. It doesn't seem to do anything that the terminal doesn't, but it does save you having to install the AWS CLI on every computer you use. 