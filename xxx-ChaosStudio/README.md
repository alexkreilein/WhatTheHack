# What The Hack - xxx-ChaosStudio

## Introduction 

Azure Chaos Studio (Preview) is a managed service for improving resilience by injecting faults into your Azure applications. Running controlled fault
injection
experiments against your applications, a practice known as chaos engineering, helps you to measure, understand, and improve resilience against real-world
incidents, such as a region outages or application failures causing high CPU utilization on a VMs, ScaleSets, and Azure Kubernetes.


## Learning Objectives
This “What the Hack” WTH is designed to introduce you to Azure Chaos Studios (Preview) and guide you through a series of hands-on challenges to accomplish
the following:
  
1. Leverage the Azure Chaos Studio to inject failure into an application/workload
2. Provide hands-on understanding of Chaos Engineering 
3. Understand how resilientcy can be achieved with Azure 

In this WTH, you are the system owner of the Contoso Pizzaria Application. Super Bowl Sunday is Contoso Pizza's busiest time of the year, the pizzaria
ordering application must be must be avaliable during the Superb Bowl. 

You have been tasked to test the resiliency of the pizzaria application. The pizzaria application is running on Azure and you will use Chaos Studio to
simulate various failures. 

## Challenges
1. Challenge 01: **[Ready Set Go](Student/Challenge-01.md)**
	 - Deploy Multi-Region Pizza (K8s based) applcation,
1. Challenge 02: **[Is your application ready for the SuperBowl?](Student/Challenge-02.md)**
	 - How does your application handle failure during large scale events?
1. Challenge 03: **[My AZ burned down, now what?](Student/Challenge-03.md)**
	 - Can your Application survive an Azure outtage of 1 or more Avialability Zones?
1. Challenge 04: **[Godzilla destroys my Azure region!](Student/Challenge-04.md)**
	 - Can your Application survive a region failure? 
1. Challenge 05: **[Injecting Chaos into your pipeline](Student/Challenge-05.md)**
	 - Description of challenge

## Prerequisites
- Azure subscription with owner access
- Visual Studio Code terminal or Azure Shell (recommended)
- Latest Azure CLI (if not using Azure Shell) 
- Github or Azure DevOps to automate Chaos Testing
- Azure fundamentals, Vnets, NSGs, ScaleSets, Traffic Manager 
- Fundamentals of Chaos Engineering
- Basic understanding of Kubernetes (kubectl commands)

## Repository Contents (Optional)
- `./Coach/Guides`
  - Coach's Guide and related files
- `./ContosoPizza`
  - Image files and code for the pizza application
- `./images`
  - Generic image files needed
- `./Student/Guides`
  - Student's Challenge Guide

## Contributors
- Jerry Rhoads
