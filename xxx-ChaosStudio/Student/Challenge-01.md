# Challenge 0: Prerequisites - Ready, Set, GO!

**[Home](../README.md)** - [Next Challenge >](./01-assessment.md)

## Pre-requisites

You will need an Azure subscription with "Owner" permissions.  

Before starting, you should decide how and where you will want to work on the challenges of this hackathon.

You can complete the entirety of this hack's challenges using the [Azure Cloud Shell](#work-from-azure-cloud-shell) in a web browser (fastest path), or you can choose to install the necessary tools on your [local workstation (Windows/WSL, Mac, or Linux)](#work-from-local-workstation).

### Work from Azure Cloud Shell

Azure Cloud Shell (using Bash) provides a convenient shell environment with all of the tools you will need to run these challenges already included such as the Azure CLI, kubectl, helm, and MySQL client tools, and editors such as vim, nano, code, etc. 

This is the fastest path. To get started, simply open [Azure Cloud Shell](https://shell.azure.com) in a web browser and you're all set!

### Work from Local Workstation

As an alternative to Azure Cloud Shell, this hackathon can also be run from a Bash shell on your computer. You can use the Windows Subsystem for Linux (WSL2), Linux Bash or Mac Terminal. While Linux and Mac include Bash and Terminal out of the box respectively, on Windows you will need to install the WSL: [Windows Subsystem for Linux Installation Guide for Windows 10](https://docs.microsoft.com/en-us/windows/wsl/install-win10).

If you choose to run it from your local workstation, you need to install the following tools into your Bash environment (on Windows, install these into the WSL environment, **NOT** the Windows command prompt!):

- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/)
- Kubectl (using `az aks install-cli`)
- [Helm3](https://helm.sh/docs/intro/install/) 
- MySQL command line client tool (or optional GUI tool mentioned below)
- PostgreSQL command line client tool (or GUI optional tool mentioned below)

You should carefully consider how much time you will need to install these tools on your own computer. Depending on your Internet and computer's speed, this additional local setup will probably take around 30-60 minutes. You will also need a text editor of your choice if it is not already installed. 

## Introduction

Now that you have your pre-requisites set up, it is time to get the hack's environment set up.  

This hack is designed to help you learn chaos testing with Azure Chaos Studio. The hack uses a pre-canned Azure Kurbernettes (AKS) environment that you will deploy into your Azure subscription. This environment as your testing target. 

The Pizza Application runs entirely on an AKS cluster in Azure, consisting of:
 - Two instances of the "Pizzeria" sample app
 - A MySQL database

## Description

The Pizza Application is deployed in two steps by scripts that invoke ARM Templates & Helm charts to create the AKS cluster, databases, and sample application.  Your coach will provide you with a Resources.zip file that contains the files needed to deploy the AKS environment.

   - Download the required Resources.zip file for this hack. You should do this in Azure Cloud Shell or in an Mac/Linux/WSL environment which has the Azure CLI installed. 
   - Unzip the Resources.zip file

### Deploy "on-prem" AKS Environment

Run the following command to setup the on-prem AKS environment:

```bash
cd ~/Resources/ARM-Templates/KubernetesCluster
chmod +x ./create-cluster.sh
./create-cluster.sh

```

   **NOTE:** Creating the cluster will take around 10 minutes

   **NOTE:** The Kubernetes cluster will consist of one container contosoappmysql. 

### Deploy the Sample Applications

Deploy the Pizza applications - it will create one web application.

```bash
cd ~/Resources/HelmCharts/ContosoPizza
chmod +x ./*.sh
./deploy-pizza.sh

```

**NOTE:** Deploying the Pizzeria application will take around 5 minutes

### View the Sample Application

Once the applications are deployed, you will see a link to a web sites running on port 8081. In Azure Cloud Shell, these are clickable links. Otherwise, you can cut and paste the URL in your web browser.
   
```bash
      Pizzeria app on MySQL is ready at http://some_ip_address:8081/pizzeria      
```

## Success Criteria

* You have a Unix/Linux Shell for setting up the Pizzeria application (e.g. Azure Cloud Shell, WSL2 bash, Mac zsh etc.)
* You have validated that the Pizzeria application is working


## Hints

* The AKS "contossoappmysql" web front end has a public IP address that you can connect to. 
* In order to obtain the public IP address, run this commands and look for the "external-IP".

```bash

 kubectl -n mysql get svc

```

There are more useful kubernetes commands in the reference section below.


## References

* [AKS cheatsheet](./K8s_cheetsheet.md)
* [pgAdmin](https://www.pgadmin.org) (optional)
* [MySQL Workbench](https://www.mysql.com/products/workbench/) (optional)
* [Azure Data Studio](https://docs.microsoft.com/en-us/sql/azure-data-studio/download-azure-data-studio?view=sql-server-ver15) (optional)
* [Visual Studio Code](https://code.visualstudio.com/) (optional)

