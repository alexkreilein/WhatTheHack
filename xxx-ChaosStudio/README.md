# What The Hack - xxx-ChaosStudio

## Introduction
This hack will help get you hands-on experience with Azure Chaos Studios (Preview). 

So what is Chaos Engineering? 

Chaos Engineering is a concept that comes from Netflix. Netflix’s video streaming platform is a “born in the cloud” application. As it is in the cloud, Netflix doesn’t have access to hardware and facilities, as such Netflix needed to to build and test resiliency in their streaming platform. Microsoft introduces Chaos Studio to measure, understand and how to improve service/workload resilience. 

Chaos Studio allows you to simulate failures at various levels of your application or workload. 

## Learning Objectives
This “What the Hack” WTH is designed to introduce you to Azure Chaos Studios and guide you through a series of hands-on challenges to accomplish the following:
  
1. Leverage the Azure Chaos Studio to inject failure into an application or workload
2. Provide hands-on understanding of Chaos Engineering
3. Understand how resilientcy is part of the Well Architected Framework

In this WTH, you are the system owner of the Contoso Pizza Application. Super Bowl Sunday is Contoso Pizza's busiest time of the year, the pizza ordering application must be must be avaliable during the Superb Bowl. 

You have been tasked to test the resiliency of the pizza application. The pizza application is on Azure and you will use Chaos Studio to simulate various failures. 

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
- Visual Studio Code (can use Azure Shell)
- Azure CLI
- Github or Azure DevOps to automate Chaos Testing
- Azure fundamentals, Vnets, NSGs, ScaleSets, Traffic Manager 
- Fundamentals of Chaos Engineering

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
- 
