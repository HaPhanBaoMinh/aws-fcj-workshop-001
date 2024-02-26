---
title: "Install CodeDeploy Agent"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: "<b>5.3 </b>"
---

Reference documentation [Here](https://docs.aws.amazon.com/codedeploy/latest/userguide/codedeploy-agent-operations-install-linux.html)

1. Update **yum** and install necessary **packages**:

        sudo yum update

        sudo yum install ruby

        sudo yum install wget

    ![EC2](/aws-fcj-workshop-001/4-EC2/14.png)

2. Navigate to the **home directory**:

        cd /home/ec2-user

3. Download the **CodeDeploy agent**:

        wget https://aws-codedeploy-ap-southeast-1.s3.ap-southeast-1.amazonaws.com/latest/install

    Currently, I am performing this in the **ap-southeast-1** region. If you are in a different region, refer to the link at the top of the page for installation instructions specific to that region.

    ![EC2](/aws-fcj-workshop-001/4-EC2/15.png)

    After installation, you will see the **install** file.

4. Grant permissions and install the **install** file:

        chmod +x ./install

        sudo ./install auto

    Installation successful.

    ![EC2](/aws-fcj-workshop-001/4-EC2/16.png)

5. Check the status of the CodeDeploy Agent:

        systemctl status codedeploy-agent

    The CodeDeploy Agent is now running successfully.

    ![EC2](/aws-fcj-workshop-001/4-EC2/17.png)
