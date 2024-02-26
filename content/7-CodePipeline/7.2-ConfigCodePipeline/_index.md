---
title: "Configuring CodePipeline"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: "<b>7.2 </b>"
---

#### Configuring CodePipeline

1. After creating the **CodePipeline**, you may encounter an error during the **Deploy** stage.

    ![CodePipeline](/images/7-CodePipeline/7.png)

2. On the **aws-ci-cd-pipeline** screen, select **Edit**.

    ![CodePipeline](/images/7-CodePipeline/8.png)

3. In the **Edit: Deploy** section, select **Edit stage**.

    ![CodePipeline](/images/7-CodePipeline/9.png)

    ![CodePipeline](/images/7-CodePipeline/10.png)

4. In the edit window:

    - Change **Input artifacts** to **Source Artifact**.

    - Select **Done**.

    ![CodePipeline](/images/7-CodePipeline/11.png)

5. Complete the process by selecting **Save**.

    ![CodePipeline](/images/7-CodePipeline/12.png)
