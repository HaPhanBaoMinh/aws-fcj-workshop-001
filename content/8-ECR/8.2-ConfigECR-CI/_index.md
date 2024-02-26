---
title: "Configure ECR for CI"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b>8.2 </b>"
---

1. We navigate to [ECR](https://ap-southeast-1.console.aws.amazon.com/ecr/private-registry/repositories?region=ap-southeast-1)

   - Copy the **URI** of the repository you just created

    ![ECR](/aws-fcj-workshop-001/8-ECR/3.png)

2. Access **CodeCommit**

    - Select **Repositories**

    - Access the repository we created **aws-ci-cd-codecommit**

    ![ECR](/aws-fcj-workshop-001/8-ECR/4.png)

    - Access the **buildspec.yml** file

    ![ECR](/aws-fcj-workshop-001/8-ECR/5.png)

    - Choose **Edit**

    - Replace all **<ECR_REPOSITORY_URI>** placeholders with the **URI** of the **ECR** repository

    - Replace all **<region>** placeholders with **ap-southeast-1**

    ![ECR](/aws-fcj-workshop-001/8-ECR/6.png)

    - After making the changes, provide necessary information

    - **Commit changes**

    ![ECR](/aws-fcj-workshop-001/8-ECR/7.png)
