# Generative AI 
This repo is adapted from the official [Generative AI on AWS repo]([https://github.com/data-science-on-aws/data-science-on-aws](https://github.com/generative-ai-on-aws/generative-ai-on-aws)) and adjusted to reflect the capabilities of AWS Learner Labs.
[![](img/gaia_book_cover_sm.png)](https://www.amazon.com/Generative-AI-AWS-Multimodal-Applications/dp/1098159225/)


# Important! :warning::warning::warning:

- In AWS Learner Labs once you reach $100 all of your code will be automatically destroyed. In addition, AWS Learner Labs has occasional issues where your environment is not accessible.
- **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
- In order to make it easy to complete labs and work on your project, it is highly reccomended that you follow the below process twice, once for a `lab` user and once for a `project` user (be sure you are saving your work from the `project` user in your own GitHub repository.


# Setup Instructions
[<img src="https://github.com/MADS508/labs/blob/main/img/youtube_screen.png" width="100%">](https://youtu.be/YY4bj1hqCGI)

## 1. Login to AWS Learner Labs

![Console](https://github.com/MADS508/labs/blob/main/img/aws_console.png)
Be sure to read the [AWS Academy Learner Lab Student Guide.pdf](https://github.com/MADS508/labs/files/12005191/AWS.Academy.Learner.Lab.Student.Guide.pdf)


## 2. Launch the AWS Lab
Within the Learner Lab Setup Guide follow the steps in the [Using Your Learner Lab](https://ole.sandiego.edu/bbcswebdav/pid-2625324-dt-content-rid-35250884_1/xid-35250884_1) section.

1. From the Dashboard select your course. Then click `modules`
![LearnerLabStep1](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep1_2.png)

2. Click `Launch AWS Academy Learner Lab`
![LearnerLabStep2](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep2_2_1.png)

3. In the top right click `Start Lab` This will take 2-3 minutes. Be sure to monitor your budget, once you reach $100 all of your code will be automatically destroyed. **Be sure that you are ALWAYS storing your code in GitHub. You will not be given extra time to complete an assignment due to your Learner Lab deleting your code.**
![LearnerLabStep3](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep3.png)

4. Once the lab has loaded you will see a green dot to the right of the AWS status, click it to open the AWS console.
![LearnerLabStep4](https://github.com/MADS508/labs/blob/main/img/LearnerLabsStep4.png)


## If the video indicates you need to attach an admin role, you can skip this step. As of Feb 2023 AWS Learner Labs no longer allows IAM role changes.

## 3. Launch SageMaker Studio

In the AWS Console search bar, type `SageMaker` and select `Amazon SageMaker` to open the service console.

Search for and select `SageMaker`
![Search Box - SageMaker](https://github.com/MADS508/labs/blob/main/img/search-box-sagemaker.png)

Select `Studio` and then click the button `Set up for organization`
![Notebook Instances](https://github.com/MADS508/labs/blob/main/img/setup.png)

Select the `Set up for organizations` option.
![Quick Start](https://github.com/MADS508/labs/blob/main/img/sm-quickstart-iam-existing-2_1.png)

For the domain name enter `lab` and click next.
![Domain Name](https://github.com/MADS508/labs/blob/main/img/LearnerLabs_domain_name.png)

For How do you want to access studio, choose Login through IAM
- Leave Who will use Sagemaker blank
- For What ML activities users will users perform, choose Use an existing role.
- Set the Default execution role to LabRole
- Choose Next.
![Users](https://github.com/MADS508/labs/blob/main/img/UsersandML.png)

For StageMaker Studio, choose SageMaker Studio - Classic
![Sagemaker Studio New](https://github.com/MADS508/labs/blob/main/img/SagemakerStudioClassic.png)

Expand the Canvas section and disable both MLOps settings and disable `Enable local file uplload`
![Canvas](https://github.com/MADS508/labs/blob/main/img/Canvas.png)

Also toggle off `Enable time series`
![Time Series](https://github.com/MADS508/labs/blob/main/img/TimeSeries.png)

For Network, choose public internet access.  Select an existing VPC and an existing subnet, then choose Next. Accept the default storage settings and choose Next, then choose Submit.
![Network](https://github.com/MADS508/labs/blob/main/img/Network.png)

On the Storage screen, leave the settings as is and click next.
![Storage](https://github.com/MADS508/labs/blob/main/img/Storage.png)

On the Review and create screen, confirm all of the settings followed the above, and click Submit.
Wait 10-15 minutes for the studio to build. It only takes this long on initial setup, in the future it will take 2-3 minutes to access an existing studio.
![Pending Studio](https://github.com/MADS508/labs/blob/main/img/studio_pending.png)

Open the studio by clicking `Domain` and then select your domain name, it should be `lab`
![Open Studio](https://github.com/MADS508/labs/blob/main/img/SelectDomain.png)

Select `User profiles` and then click `Add user`
![Add User](https://github.com/MADS508/labs/blob/main/img/AddUser.png)

Leave the `General Settings` as is, execution role must be `LabRole`, click next.
![User step 1](https://github.com/MADS508/labs/blob/main/img/User1.png)

Leave `Studio settings` as is and click next.
![User step 2](https://github.com/MADS508/labs/blob/main/img/User2.png)

Leave `RStudio settings` as is and click next.
![User step 3](https://github.com/MADS508/labs/blob/main/img/User3.png)

Turn off the following and then click `submit`
- Enable Canvas base permissions
- Enable Canvas Ready-to-use models
- Enable document query using Amazon Kendra
- Enable time series forecasting
- Both ML Ops Configuration settings
![User step 4](https://github.com/MADS508/labs/blob/main/img/User4.png)

Now click `Launch` and select `Studio`
![Launch](https://github.com/MADS508/labs/blob/main/img/Launch.png)

Wait 2-3 minutes for the studio to launch.
![Loading Studio](https://github.com/MADS508/labs/blob/main/img/studio_loading.png)


## 4. Launch a New Terminal within Studio
Click `File` > `New` > `Terminal` to launch a terminal in your Jupyter instance.
![Terminal Studio](https://github.com/MADS508/labs/blob/main/img/studio_terminal.png)


## 5. Clone this GitHub Repo in the Terminal
Within the Terminal, run the following:
```
cd ~ && git clone -b main https://github.com/scoyne2/generative-ai-on-aws.git

```

If you see an error like the following, just re-run the command again until it works:
```
fatal: Unable to create '.git/index.lock': File exists.

Another git process seems to be running in this repository, e.g.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.
```
_Note:  Just re-run the command again until it works._
