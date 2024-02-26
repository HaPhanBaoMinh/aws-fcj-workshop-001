---
title: "Assign IAM for CodeBuild"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b> 4.3 </b>"
---

#### Assign IAM for CodeBuild

1. Access **CodeCBuild** and select **Service role**.

    ![CodeCBuild](/images/3-CodeBuild/11.png)

2. You will be directed to the service role of CodeBuild.

   - Choose **Add permissions**.

   - Select **Attach policies**.

    ![CodeCBuild](/images/3-CodeBuild/12.png)

    - Search and select **IAM_CODEDBUILD_CICD** that we created.

    - Click **Add permissions**.

    ![CodeCBuild](/images/3-CodeBuild/13.png)

3. Policy added successfully.

    ![CodeCBuild](/images/3-CodeBuild/14.png)
