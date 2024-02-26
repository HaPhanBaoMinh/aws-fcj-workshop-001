---
title : "Tạo IAM cho CodeBuild"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 4.2 </b> "
---

#### Tạo IAM cho CodeBuild

1. Truy cập **IAM**

    - Chọn **Policies**

    - Chọn **Create policy**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/7.png)

2. Màn hình **Create policy**

    - Phần **Service** Chúng ta tìm **Elastic Container Registry**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/8.png)

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

    - Chuyển sang định dạng **JSON** và điền 1 số quyền cần thiết để **CodeBuild** có thể thao tác với **ECR**

    - **Next**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/9.png)

    - Phần **Policy name** điền **```IAM_CODEDBUILD_CICD```**

    - Chọn **Create policy**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/10.png)




