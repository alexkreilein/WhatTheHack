
## Introduction 
When customers experience our products, they experience both our success and our failure. For developers building mission critical applications, customers often have higher expectations of quality management that we might expect. The nature of the end-users use of the application requires our work to be rugged, resistent to failure, and recoverable when failures do inevitably happen.

Our goal is to empower developers to find likely and consequential failures in their applications early, often, and effectively. By adopting chaos engineering and stress testing as part of a test-driven-development process in a continuous validation lifecycle, developers will receive fast feedback to help them improve the quality and resiliency of their applications while increasing their release velocity. This helps to iterate quickly on challenging areas that impact the customer experience by finding issues before them become problems, empowering developers to focus on what matters, allowing them to build increasingly stable, trustworthy, and provably resiliency applications over time.

## Methodology
Microsoft Azure has released two new features that support our goals: Azure Chaos Studio (Preview) and Azure Load Testing (Preview). In this What The Hack, we will focus on learning how to use both tools and integrate them into our CI/CD pipelines for future use.

## Learning Objectives
1. Leverage a cloud-based load testing service with high fidelity support for JMeter and new/existing JMeter scripts
2. Provide a hands-on understanding of chaos engineering and automated fault injection to identify weaknesses
3. Integrate with CI/CD workflows for automated, collaborative load-testing
4. Understand how resiliency can be achieved with Azure 

## Challenges
1. Challenge 01: **[Ready Set Go](Student/Challenge-01.md)**
	 - Deploy the multi-region Kurbernetes pizzeria application

2. Challenge 02: **[Develop a Load Testing Strategy](Student/Challenge-01.md)**
	 - How to develop a load testing strategy for your application

3. Challenge 03: **[Is your application ready for the SuperBowl?](Student/Challenge-02.md)**
	 - How does your application handle failure during large scale events?

4. Challenge 04: **[Deploy Sample App & Create Load Testing Script](Student/Challenge-02.md)**
	 - Deploy a sample application and create JMeter scripts to support your load testing strategy

5. Challenge 05: **[Create Azure Load Testing Service and Establish Baselines](Student/Challenge-03.md)**
	 - Create Azure Load Testing Service and learn techniques on how to establish baselines for your application

6. Challenge 06: **[Identify & Remediate Bottlenecks](Student/Challenge-05.md)**
	 - Reviewing load test results and identifying bottlenecks

7. Challenge 07: **[Stress Testing](Student/Challenge-06.md)**
	 - How to perform stress tests and observing your application behavior

8. Challenge 08: **[My AZ burned down, now what?](Student/Challenge-03.md)**
	 - Can your application survive an Azure outtage of 1 or more Avialability Zones?

9. Challenge 09: **[Godzilla takes out an Azure region!](Student/Challenge-04.md)**
	 - Can your application survive a region failure? 

10. Challenge 10: **[Load Testing During Chaos Experiment](Student/Challenge-07.md)**
	 - Incorporating load testing and chaos experiments together

11. Challenge 11: **[Enable Automated Load Testing (CI/CD)](Student/Challenge-04.md)**
	 - Incorporating load testing into your CI/CD Pipeline

12. Challenge 12: **[Injecting Chaos into your pipeline](Student/Challenge-05.md)**
	 - Optional challenge, using Chaos Studio experiments in your CI/CD pipeline

## Prerequisites
- Azure subscription with owner access
- Visual Studio Code terminal or Azure Shell (recommended)
- Familiarity with the fundamentals of load testing
- GitHub or Azure DevOps to automate load and chaos testing in your CI/CD pipelines.
- [Apache JMeter](https://jmeter.apache.org/usermanual/get-started.html) installed on your local machine or in a VM to create your load testing script.
- [Azure Cloud Shell](https://shell.azure.com) or [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
- Azure fundamentals, Vnets, NSGs, ScaleSets, Traffic Manager 
- Basic understanding of Kubernetes (kubectl commands)

## Contributors
- Andy Huang
- Jerry Rhoads
- Kevin Gates
- Tommy Falgout 
- Alex Kreilein


