# CI-CD-Pipeline-with-cloudformation-and-github-actions
This is my first Case study with cloudformation (this project is actually a Single-tier-Application)
steps are below
- creat a repository
- creat a cloudformation template
- push the code
- Before pushing the code make sure you open your aws console and give an IAM cloudformation full access permision to the user .
- add permision from your aws console
-c onnect your aws to your github by adding the access key and the secret key of your aws account. 
    opening your github account, open the repository you are working with, go to setting, go to secret then take action, add your access key and secret key.
- under my cloudformation.yaml i have just edited the bucket name, and the stack name
-test the project by checking your aws console to see if it created the stack 

this immage indicate that the project deployed successfully
![deployed stack](https://user-images.githubusercontent.com/116527791/235388356-99ae3b7e-76b3-4584-9b16-413bd01b888d.jpg)


answers to open questions.
1. What is Github Actions and how does it integrate with CloudFormation to automate resource provisioning on AWS?
        
    GitHub Actions is a feature of the popular source code management platform 
GitHub that allows developers to automate various tasks related to their software development workflows. It enables users to define custom workflows as code directly in their repositories and run them automatically on GitHub-hosted virtual machines or their own infrastructure.
    
    Amazon Web Services (AWS) CloudFormation is a service that helps users 
 model and provision AWS resources with code. Users can use AWS CloudFormation templates to define a stack of AWS resources, such as Amazon Elastic Compute Cloud (Amazon EC2) instances, Amazon Relational Database Service (Amazon RDS) databases, and Amazon Simple Storage Service (Amazon S3) buckets, and automate their deployment and management.

    GitHub Actions can be used to trigger AWS CloudFormation stacks in response 
to various events, such as changes to the code base or pull requests. This integration allows developers to define workflows that use AWS CloudFormation templates to create, update, or delete AWS resources in response to events. Developers can define workflows as code, which can be version-controlled, shared, and reused, and use prebuilt actions from the GitHub Marketplace or build custom actions to achieve complex workflows.

    For example, a GitHub Action workflow can be defined to trigger the 
creation of an AWS CloudFormation stack that provisions an Amazon EC2 instance whenever a new pull request is opened. The workflow can also include additional steps to validate the stack, run tests on the instance, and tear down the stack when the pull request is closed. This integration streamlines the process of provisioning and managing AWS resources and makes it easier for developers to automate their software development workflows.


2. What happens if there is an error in the CloudFormation template during the pipeline execution?

    If there is an error in the CloudFormation template during the pipeline 
execution, the pipeline will fail and stop executing. Depending on the pipeline configuration, the pipeline may also trigger a notification to alert the developers or DevOps team of the failure.

    When a pipeline fails due to an error in the CloudFormation template, the 
error message will be displayed in the pipeline logs, allowing developers to identify the issue and resolve it. Common reasons for errors in CloudFormation templates include syntax errors, invalid parameter values, or resource conflicts.

    To prevent errors in CloudFormation templates from impacting the 
pipeline execution, developers can use features such as rollback triggers and stack policies to ensure that failed updates or deployments are automatically rolled back or prevented from occurring. Developers can also use testing and validation tools to identify and fix errors in the template before deploying it in the pipeline.

3. What happens if the pipeline fails during deployment

    If the pipeline fails during deployment, it means that the changes to the 
infrastructure or application being deployed were not successful. Depending on the pipeline configuration, the failure could trigger an automatic rollback or require manual intervention to address the issue.

    When a pipeline fails during deployment, the failure message will be 
displayed in the pipeline logs, providing developers with insight into the root cause of the issue. Common reasons for pipeline failures during deployment include misconfiguration, resource conflicts, and dependencies that were not properly accounted for.

    To address a pipeline failure during deployment, developers will need 
to identify and resolve the underlying issue before attempting to redeploy. This may involve making changes to the infrastructure code, modifying configuration settings, or updating dependencies. Depending on the severity of the issue, it may be necessary to roll back the deployment to the previous state to avoid any negative impact on the application or infrastructure.