# Student id : 8933139
# Student name : Dhaval Patel  
# student-id-8933139-final-proj-cloud-arc

This repository helps creating terraform backend on s3 bucket.

## Prerequisites
1) AWS cli
2) Terraform setup and running
3) git cli installed

## Backend Initialization & deloyment

1) aws configure , this command helps connect to aws from command prompt
2) S3 bucket to be created before hand to initialize backend
    <command : aws s3api create-bucket --bucket tf-state-student-id-8933139-prog8870-final-assignment-v1.1 --region us-east-1>
    bucket name : tf-state-student-id-8933139-prog8870-final-assignment-v1.1
    region : us-east-1
3) terraform init, initialize backend with below command

    <terraform init -backend-config="C:\dhaval\CloudArchitecturesandInfrastructureasCode\final_project\student-id-8933139-final-proj-cloud-arc\backend-config.hcl">
    give complete path of backend config file.

4) terraform plan -var-file="vars.tfvars"

    With this command terraform plan is executed, which validated tarraform config and files.

5) terraform apply -var-file="vars.tfvars"

    Resources are deployed with this command, post execution of this command we can check and verify if resources are deployed correctly and tfstate file is stored in S3 bucket initialized earlier.


## References 
## Terraform Documentation: https://registry.terraform.io/
## AWS Free Tier: https://aws.amazon.com/free/
## GitHub Guides: https://guides.github.com/