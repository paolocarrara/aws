## aws
I know, it's a pretty long list of steps, but I assure you, it's gonna good experience.

## Amazon Web Services The Right Way

## Conventions
The convention to name all of your resources at aws will be this:
> environment.domain.appname.[resource]

### Creating the access key to access your ec2 instances

For example:
> dev.www.nusher

Save your access key in a safe place.

### Creating the bucket to hold all your project related files.

Go to S3 service and create a new bucket with the same name of your project

For example:
> nusher

In the case that the project name is already being used by another user, well, fuck it, name it whatever you want.

### Creating the code repository
You need to have a private or public repository at GitHub or at AWS Codecommit, doesn't matter which one, just create one and push your code to the repository.

### Configuring the Docker image.
The docker image will be used in the build process. So, for example, if we have an angular we need a image with angular installed in it. Create a docker image with your project build dependencies.
If you don't know how to configure a docker image read this.


### Creating the necessary permissions and roles.
