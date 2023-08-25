
# CICD PIPELINE

Building A End to End Continuous Integration and Continuous Deployment System on AWS Services

A simple Program made in Flask was used to Build the project. The Program Simplly
print "Hello World' String


## Features

- Automatic Updates: It automatically makes sure your program is up to date when you change it.
- Testing Help: It checks your program to see if it works right and tells you if there are problems.
- Easy Sharing: It helps you easily share your program with others so they can use it too.
- Quick Fixes: If something goes wrong, it helps you quickly fix it and go back to how it was before


## Result



https://github.com/vedant990/CICD-PIPELINE/assets/121371568/f2139eff-3a38-4261-b390-6a3d4688f6b0




##  CI/CD (Continuous Integration and Continuous Deployment)

CI/CD is a set of practices that help developers automatically build, test, and deploy their software. It ensures that changes are quickly and safely delivered to users. CI (Continuous Integration) focuses on regularly combining code changes, while CD (Continuous Deployment/Delivery) automates the process of putting new code into action. This helps in faster development, fewer errors, and more reliable software.

## Instructions :
- -Create an account on https://docker.io (Keep username and password handy)

Fork The Repo or Create One with Any Name you want

```
git clone https://github.com/vedant990/cicd-code
```

- Edit The Buildspec.yml as Shown:

```
"$DOCKER_REGISTRY_PASSWORD" : Relapce With docker.io password
"$DOCKER_REGISTRY_USERNAME" : Relapce With docker.io username
"$DOCKER_REGISTRY_URL"      : Relapce with docker.io
```

You can also use AWS System Manager to Store the Crededtional

```
  parameter-store:
    DOCKER_REGISTRY_USERNAME: /myapp/docker-credentials/username
    DOCKER_REGISTRY_PASSWORD: /myapp/docker-credentials/password
    DOCKER_REGISTRY_URL: /myapp/docker-registry/url
```
- NOTE : 


```  
build:
    commands:
      - echo "Running tests..."
      - cd

      EDIT THE CD WITH THE DIRECTORY WHERE CODE WILL BE PRESENT OR ELSE KEEP EMPTY
```
  
Replace with your Own Field or Create your Own .Dont Forget to Add IAM roles with proper Policies If u are using System Manager


Appsec.yml will be used for Code Deploy



![Logo](https://a0.awsstatic.com/main/images/logos/aws_logo_smile_1200x630.png)

