---
title: "Create IAM for EC2"
date: "`r Sys.Date()`"
weight: 5
chapter: false
pre: "<b> 5.5 </b>"
---

1. Access [IAM](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/home)

    - Select **Policies** and then click **Create policy**.

    ![IAM](/aws-fcj-workshop-001/4-EC2/20.png)

2. **Create policy** screen:

    - Under **Select a service**, search for **Elastic Container Registry** - **ECR**, as the **EC2** instance needs permissions to access and retrieve images from **ECR** created by **CodeBuild**.

    - Switch to the **JSON** format and select the following permissions:

    - Then click **Next**.

            {
                    "Version": "2012-10-17",
                    "Statement": [
                            {
                            "Effect": "Allow",
                            "Action": [
                                    "ecr:GetAuthorizationToken",
                                    "ecr:BatchCheckLayerAvailability",
                                    "ecr:GetDownloadUrlForLayer",
                                    "ecr:GetRepositoryPolicy",
                                    "ecr:DescribeRepositories",
                                    "ecr:ListImages",
                                    "ecr:DescribeImages",
                                    "ecr:BatchGetImage",
                                    "ecr:GetLifecyclePolicy",
                                    "ecr:GetLifecyclePolicyPreview",
                                    "ecr:ListTagsForResource",
                                    "ecr:DescribeImageScanFindings",
                                    "s3:Get*",
                                    "s3:List*",
                                    "s3:Describe*"
                            ],
                            "Resource": "*"
                            }
                    ]
            }

    ![IAM](/aws-fcj-workshop-001/4-EC2/22.png)

    - Enter the **Policy name** as **```IAM_EC2_CICD```** and click **Create policy**.

    ![IAM](/aws-fcj-workshop-001/4-EC2/23.png)

3. Grant permissions to [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false)

    - Select **EC2**.

    - Choose **Actions**.

    - Select **Security**.

    - Choose **Modify IAM role**.

    ![EC2](/aws-fcj-workshop-001/4-EC2/24.png)

4. **Modify IAM role**:

    - Select the **IAM role** created in the previous step, **IAM_EC2_CICD**.

    - Click **Update IAM role**.

    ![EC2](/aws-fcj-workshop-001/4-EC2/25.png)
