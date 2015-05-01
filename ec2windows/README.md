Example EC2 Windows
-------------------

This is a sample ClearCode application template and tasks for Deploy. It demonstrates the booting of a single Windows server in AWS EC2, configuring the server and installating software, then running tests and terminating the server. 

Importing the Template and Tasks
--------------------------------

To import this deployment template, clone this repository or download the full repository and unzip the resulting tarball to a server with the ClearCode Client command line tools already configured with your ClearCode server. 

Next run the following command to import this Deploy Template, pointing to the directory that contains this readme file.    

    ccl-import-application-template --inputdirectory ec2windows --makeavailable

Prerequisites
-------------

This tutorial assumes that you are familiar with Amazon AWS EC2, have an account and have access to the AWS Console. Certain information will need to be gathered before starting this tutorial:

* AWS API key and secret key with the ability to start and terminate EC2 instances, create and delete security groups
* Select an EC2 Region (default in walkthrough is us-east-1)
* A Windows Server 2012 base image in that region (default in walkthrough is ami-cc93a8a4 in us-east-1)

> NOTE: In this tutorial we will use EC2 Classic Security Groups for simplicity's sake (not VPC)

You may want to go through the walk through for the standalone Automate Task sample linked below. This Deploy sample is based on that task and has all the same prerequisites and more indepth explanations of the task steps.

https://github.com/clearcode-labs/automate-samples/tree/master/ec2winrm

Setup Cloud Credentials
-----------------------

Before beginning with importing and running the task, you must setup the AWS credentials in ClearCode. See http://docs.clearcodelabs.com/docs/automate/cloud/cloud-account.html

Running
-------

To start this Deployment, in the ClearCode user interface navigate using the right menu: `Deploy, Home`. Select the `shopping cart` on the left. Then click `Deploy` next to "Example EC2 Windows". CLick through the dialogue to launch the start sequence. 

The Start sequence will launch Windows Server 2012 server in Amazon EC2, us-east-1. Once the start sequence is completed, go to the `Management` tab on the Deployment page and run the `Tests` sequence. This will test that the software was successfully installed. Lastly run the `Terminate` sequence to clean things up in EC2.
