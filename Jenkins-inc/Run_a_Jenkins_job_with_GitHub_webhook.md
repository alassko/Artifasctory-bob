Run a Jenkins job with GitHub webhook
pre-requisites
A Jenkins Server Click here for help
A GitHub repository Click here for help
Integration Steps
Log into the Jenkins

Create a Freestyle Project
Create a new job
Job Name : WebhookTestJob

Source code management
Git URL : get URL here
Build Triggers
 GitHub hook trigger for GITScm polling
Build --> Add Build Step --> Invoke Top Level Maven Triggers

Maven Version: Maven
Goals: clean install
On GitHub repository

repository --> settings --> webhooks

Add webhook
Payload URL : Jenkins_IP>:8080/github-webhook/
Content type : Application/JSON
Update the code with new commit. It should trigger our job in the jenkins
