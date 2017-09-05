## aws
This is a guide on how to deploy an application to Amazon Web Services (AWS).

This guide assumes that you already have an account and knows what AWS is used for.

The guide will walk you through the implementation of a continuos integration and continuous deploy using most of the the AWS resources.

If you feel read move the Wiki pages, there we will start the process step by step. Good Luck!

### The general resources that will be used are:
#### Elastic Container (EC2)
> It will be used to run our application.

#### Elastic Container Registry (ECR)
> It will be used to save or docker image. One could opt to use the docker hub.

#### Code Commit [optional]
> It will hold our code, just like GitHub, Bitbucker and many others do.

#### Code Build
> It will build our code. It means that the code build will get our last committed code, run the necessary build steps and save the build artifacts (files to be served) in to S3.

#### Code Deploy
> It will get the built code that is saved to S3 and put it inside our EC2 instances to be served by apache or nginx.

#### Code Pipeline
> It will automate all the process for us. If we don't use it we will have to do the build and deploy commands manually.

#### Identity and Access Management (IAM)
> It will be used to create users and access keys. The access key will be used to access our instances by ssh.

#### Elastic Load Balancer (ELB)
> It will be used to help us to distribute the connections all over our instances.

#### Launch Configurations
> It will be used to define how we want our instances to be launched when the need comes. The need generally comes from a set of rules that we will define later. The service used to verify if the need arrived is the Auto Scaling Groups.

#### Auto Scaling Groups
> It will be used to scale our application size horizontally, i.i.e, it will replicate our app across multiple instances if the a given rule is met. It will scaled down too, if a rule that was previously met goes to an unsatisfied state.

#### Amazon S3 (S3)
> It will hold our build artifacts.

#### Amazon Machine Image (AMI)
> It will be used to hold wall the external software needed by our application to run, example: Apache.

#### GitHub [optional]
> It will hold our code, one could use Code Commit.

#### Docker
> It will be used to assembly an image that we can use to build our project.
