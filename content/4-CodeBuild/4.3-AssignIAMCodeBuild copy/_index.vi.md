---
title : "Gán IAM cho CodeBuild"
date :  "`r Sys.Date()`" 
weight : 3
chapter : false
pre : " <b> 4.3 </b> "
---

#### Tạo IAM cho CodeBuild

1. Truy cập **CodeCBuild** và chọn **Service role**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/11.png)

2. Chúng ta sẽ được chuyển tới service role của CodeBuild

   - Chúng ta chọn **Add permissions**

   - Chọn **Attach policies**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/12.png)

    - Chúng ta tìm kiếm và tích chọn **IAM_CODEDBUILD_CICD** mà chúng ta đã tạo

    - Chọn **Add permissions**

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/13.png)

3. Đã thêm policy thành công

    ![CodeCBuild](/aws-fcj-workshop-001/3-CodeBuild/14.png)
