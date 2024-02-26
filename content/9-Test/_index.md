---
title: "Check the Results"
date: "`r Sys.Date()`"
weight: 9
chapter: false
pre: "<b>9. </b>"
---

1. We access **CodeCommit**

    ![Test](/aws-fcj-workshop-001/9-Test/1.png)

2. On the **aws-ci-cd-pipeline** screen

    - Select **Release change**

    - Choose **Release**

    ![Test](/aws-fcj-workshop-001/9-Test/2.png)

3. Wait for the results

    - Monitor each step

    ![Test](/aws-fcj-workshop-001/9-Test/3.png)

4. After all steps are successful, we return to **EC2** and access the **Public IPv4 address**

    - Make sure to access using **http**

    ![Test](/aws-fcj-workshop-001/9-Test/4.png)

5. Result

    ![Test](/aws-fcj-workshop-001/9-Test/5.png)

6. Let's try changing the code in the **CodePipeline** to trigger the CI/CD process automatically

    - Access **aws-ci-cd-codecommit / views / index.pug**

    - Let's try changing the content of the **h1** tag

    - Then fill in the information and **Commit**

    ![Test](/aws-fcj-workshop-001/9-Test/6.png)

    ![Test](/aws-fcj-workshop-001/9-Test/7.png)

7. After **Commit**, when we go back to **CodePipeline** we can see the status has changed to **In progress**

    ![Test](/aws-fcj-workshop-001/9-Test/8.png)

8. When all steps are successful, return to access the **Public IPv4 address** of **EC2**

    ![Test](/aws-fcj-workshop-001/9-Test/9.png)
