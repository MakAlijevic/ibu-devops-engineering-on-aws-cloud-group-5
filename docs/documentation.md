# Approach

## Phase 1

In the first phase of the project,we developed our initial plan and created an infrastructure diagram as seen on the image below.
<img src=/docs/image.png alt=diagram style="margin-bottom: 4px;" />

We also estimated the cost of the proposed solution, which we created using AWS Pricing Calculator :

Open <a href="/docs/My Estimate - AWS Pricing Calculator.pdf" target="_blank">here</a>

## Phase 2

In this phase, our focus was on constructing the solution. The goal was to develop a highly available, highly scalabe and secure web application.

To accomplish that, we have completed the following steps:

1. Created a Virtual Private Cloud (VPC) to host the application.
2. Created 4 Subnets: By creating 4 subnets, we have divided our VPC into smaller segments to segregate and organize resources. We created two public and two private subnets into two different avilability zones.
3. Created 2 route tables, which defined where the traffic should be directed.
4. Created an Internet Gateway.
5. Created a Public Security Group.

## Phase 3

In this phase, we created our virtual machine using a computing service - Amazon Elastic Compute Cloud (Amazon EC2).
We created two EC2 instances, for each availability zone.

We have also set up an RDS database, which can only be accessed from the EC2 instances we created.
Additionaly, we have created a Cloud9 environment that has access to both the RDS database and the EC2 instances, providing a unified development and management environment.

Lastly, we tested the deployment of the web application, ensuring that our application has all the necessary functionalities and that they work as expected. Most importantly, we ensured that it is accessible from the internet.

## Phase 4

To achieve high availability and scalability of our web application, we launched a Load Balancer. The purpose of a Load Balancer is to evenly distribute incoming network traffic across multiple instances of our application, ensuring optimal performance, efficient resource utilization, and increased fault tolerance.

We created a launch template that replicated our EC2 instance, allowing us to access our web application.

Lastly, we tested our application once again, and we were satisfied and happy with the results.
