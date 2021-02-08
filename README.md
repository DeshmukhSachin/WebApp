# Example WebApp

This application is an  web application written in Go. Source code is unavailable.

# Deployment Pipeline

This GitHub repo is linked with an AWS account. When a new version of ApptioWebApp.zip is checked in, the AWS Code Pipeline is triggered which in turn calls AWS CodeDeploy to deploy the artifacts on an Linux EC2 machine using codedeploy agent.

The AppSpec.yml under "Bin" folder has the instructions for AWS Code Deploy.

# How to deploy this webapp

    Manually
      Copy the static files under Public folder on your EC2 machine
      Copy the binary file (example-webapp-linux) to your EC2 machine
      Execute the binary "./example-webapp-linux"
      This will start a webapp listening on port 3000
      
   Automatic
      Make a pull request to the main branch (The Webapp is deployed as a zipped artifact, ApptioWebApp.zip is an example)
      This will trigger AWS CodePipeline and AWS CodeDeploy services on the linked AWS account
      CodeDeploy agent installed on EC2 machine will use the appspec.yml instructions to deploy the webapp
      

