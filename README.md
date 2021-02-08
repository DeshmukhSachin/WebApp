# Example WebApp

This application is an  web application written in Go. Source code is unavailable.

# Deployment Pipeline

This GitHub repo is linked with an AWS account. When a new version of ApptioWebApp.zip is checked in, the AWS Code Pipeline is triggered which in turn calls AWS CodeDeploy to deploy the artifacts on an Linux EC2 machine using codedeploy agent.

The AppSpec.yml under "Bin" folder has the instructions for AWS Code Deploy.

# How to deploy this webapp

1. Check out the ApptioWebApp.zip


