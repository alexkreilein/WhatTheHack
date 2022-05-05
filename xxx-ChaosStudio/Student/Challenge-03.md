# Challenge 03 - Can your Application Survive an Availablity Zone Failure

**[Home](../README.md)** - [Next Challenge >](./Challenge-02.md)

## Introduction

Welocme to Challenage 3. How did your application do with pod failures? Are you still in business? Now that you have tested for pod faults and have overcome with resiliency --it is time to kick it up to the next level. Winter storms are a possiblity on Superbowl Sunday and you need to prepare for an Azure datacenter going offline. Choose your prefered region and AKS cluster to simulate an Avalability Zone failure. 
 

## Description

As the purpose of this WTH is to show Chaos Studio, we are going to pretend that an Azure Avalability Zone (datacenter) is offline. The way you will simulate this will be failing an AKS node with Chaos Studio. 

- Create and Chaos Experiment to fail 1 of the pizza application's virtual machine(s)

## Food for thought

- During the experiment, were you able to order a pizza? 
- If not, what could you do to make your application resiliant at the Avalability Zone / Virtual Machine layer? 

## Hints

-  Take note of your virutal machine's instanceID
-  Verify where your pods are running (Portal or CLI)

```bash
kubectl get pods --all-namespaces -o wide --field-selector spec.nodeName=<node>

```

-  All virtual machine scaling should be done via AKS (not at the scale set)

## Success Criteria

- Chaos Experiment fails the node running the pizzeria application
- Observe any failure
- Scale AKS cluster 
- Scale the application to run on 2 virtual machines
- Re-run Chaos Experiment
- Application is functioning 


## References 
- [scale AKS cluster] (https://docs.microsoft.com/en-us/azure/aks/scale-cluster)
- [AKS cheatsheet](./K8s_cheetsheet.md)

