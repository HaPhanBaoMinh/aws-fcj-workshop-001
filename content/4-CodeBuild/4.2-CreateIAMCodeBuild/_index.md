---
title: "Create IAM for CodeBuild"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b> 4.2 </b>"
---

#### Create IAM for CodeBuild

1. Access **IAM**:

    - Select **Policies**.

    - Choose **Create policy**.

    ![CodeCBuild](/images/3-CodeBuild/7.png)

2. **Create policy** screen:

    - In the **Service** section, search for **Elastic Container Registry**.

    ![CodeCBuild](/images/3-CodeBuild/8.png)

        {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Effect": "Allow",
                    "Action": [
                        "ecr:CompleteLayerUpload",
                        "ecr:GetAuthorizationToken",
                        "ecr:UploadLayerPart",
                        "ecr:InitiateLayerUpload",
                        "ecr:BatchCheckLayerAvailability",
                        "ecr:PutImage"
                    ],
                    "Resource": "*"
                }
            ]
        }

    - Switch to the **JSON** format and enter the necessary permissions for **CodeBuild** to interact with **ECR**.

    - Click **Next**.

    ![CodeCBuild](/images/3-CodeBuild/9.png)

    - For **Policy name**, enter **```IAM_CODEDBUILD_CICD```**.

    - Select **Create policy**.

    ![CodeCBuild](/images/3-CodeBuild/10.png)
