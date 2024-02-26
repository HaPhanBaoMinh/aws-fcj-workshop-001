---
title : "Tạo IAM cho EC2"
date :  "`r Sys.Date()`" 
weight : 5
chapter : false
pre : " <b> 5.5 </b> "
---

1. Truy cập [IAM](https://us-east-1.console.aws.amazon.com/iam/home?region=ap-southeast-1#/home)

    - Chọn **Policies** sau đó chọn **Create policy**

    ![IAM](/images/4-EC2/20.png)

2. Màn hình **Create policy**

    - Ở mục **Select a service** ta tìm kiếm service **Elastic Container Registry** - **ECR**, vì **EC2** cần
     một số quyền để truy cập và lấy các images trong **ECR** được tạo ra từ **CodeBuild**

     - Các bạn chuyển qua định dạng **JSON** chọn các quyền sau

     - Sau đó chọn **Next**
        
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

    ![IAM](/images/4-EC2/22.png)

    - Điền tên **Policies** là **```IAM_EC2_CICD```** và chọn **Create policy**

    ![IAM](/images/4-EC2/23.png)

3. Tạo **EC2 Role** và gắn **policy** vừa tạo

    - Chọn **Roles**

    - Chọn **Create role**

    ![IAM](/images/4-EC2/27.png)

    1. **Step 1**

        - Chọn **AWS service**

        - Tìm kiếm và chọn service **EC2**

        - Phần **Use case** chọn **EC2**

        - **Next**

        ![IAM](/images/4-EC2/28.png)
    
    2. **Step 2**

        - Các bạn tìm kiếm policy mà các bạn đã tạo **IAM_EC2_CICD**

        - **Next**

        ![IAM](/images/4-EC2/29.png)

    3. **Step 3**

        - Phần **Role name** điền **```EC2_CICD_Role```**

        - **Create role**

        ![IAM](/images/4-EC2/30.png)


4. Gán quyền cho [EC2](https://ap-southeast-1.console.aws.amazon.com/ec2/home?region=ap-southeast-1#Instances:v=3;$case=tags:true%5C,client:false;$regex=tags:false%5C,client:false)

    - Chọn **EC2**

    - Chọn **Actions**

    - Chọn **Security**

    - Chọn **Modify IAM role**

    ![EC2](/images/4-EC2/24.png)

5. **Modify IAM role**

    - Chọn **IAM role** mà chúng ta đã tạo ở bước trước đó **IAM_EC2_CICD**

    - **Update IAM role**

    ![EC2](/images/4-EC2/25.png)




