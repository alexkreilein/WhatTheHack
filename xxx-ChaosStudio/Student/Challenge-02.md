# Challenge 02 - Is your Application Resilent?

**[Home](../README.md)** - [Next Challenge >](./Challenge-02.md)

## Introduction

In this part of the Hack, this is where the rubber meets the road. It is Super Bowl Sunday and you are the system owner of Contoso Pizza's pizza ordering workload. This workload is hosted in Azure's Kubernettes Service (AKS). 
SuperBowl Sunday is Contoso Pizza's busiest day of the year. 
To make Super Bowl Sunday a success, your job is to plan for possible failures that could occur during the Superbowl event.  
 

## Description

Create failure at the AKS pod level in your prefered region e.g. EastUS

- Prepare environment for AKS failures 
- Load and scope Chaos Experiment to the workload's web tier

## Food for thought

- During the experiment, were you able to order a pizza? 
- If not, what could you do to make your application resiliant at the POD layer?  

## Hints

- verify the the "selector" in the experiment uses namespace of the application
- Command to view the private and public IP of the pizza application 

```bash
kubectl get -n contosoappmysql svc

```

- Command to view all names spaces running in the AKS cluster

```bash
kubectl get pods --all-namespaces

```

- Command to view all names spaces running in the AKS cluster

```bash
kubectl scale deployment -n APPNAME NAMESPACE --replicas=2

```

## Success Criteria

- Loaded Chaos Mesh on Cluster
- Verify Pod Chaos restarted the application's AKS pod
- Add Resliancy to the AKS pods
- Verified Pizza Application was avalable during pod restarts

## References 
[Simulate AKS pod failure with Chaos Studio](https://docs.microsoft.com/en-us/azure/chaos-studio/chaos-studio-tutorial-aks-portal)
[AKS cheatsheet](./K8s_cheetsheet.md)


