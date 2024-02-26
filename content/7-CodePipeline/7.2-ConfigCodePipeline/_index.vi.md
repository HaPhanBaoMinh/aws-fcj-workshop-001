---
title : "Config CodePipeline"
date :  "`r Sys.Date()`" 
weight : 2
chapter : false
pre : " <b> 7.2 </b> "
---

#### Config CodePipeline

1. Sau khi đã tạo xong **CodePipeline** sẽ thực hiện quá trình nhưng sẽ gặp lỗi ở bước **Deploy**

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/7.png)

2. Ở màn hình **aws-ci-cd-pipeline** chúng ta chọn **Edit**

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/8.png)

3. Ở phần **Edit: Deploy** chúng ta chọn **Edit stage**

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/9.png)

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/10.png)

4. Ở cửa sổ edit

    - Mục **Input artifacts** chúng ta đổi thành **Source Artifact**

    - Chọn **Done**

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/11.png)

5. Hoàn tất quá trình chọn **Save**

    ![CodePipeline](/aws-fcj-workshop-001/-workshop-001/-workshop-001/-workshop-001/-workchop-001j-workshop-001/7-CodePipeline/12.png)