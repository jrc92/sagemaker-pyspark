# sagemaker-pyspark

This ```README.md``` document outlines how to setup your SageMaker notebook instance, link it to your GitHub and push changes to GitHub


## Step 1
In the AWS Console, search for 'Amazon SageMaker'. Proceed to create a notebook by clicking on 'Create Notebook Instance'.
* choose an instance type of 'ml.m4.xlarge', which is the instance type we are using for the MNIST-pyspark notebook
* for your IAM role, create a 'create new IAM role' with the default settings 


## Step 2
To connect your Git repository to the notebook instance, during the notebook instance creation process in Step 1, you'll be able to link your GitHub at the Git Repository tab
* Choose 'Add a Repository to SageMaker'
* Proceed to create the repository at GitHub and copy-pasting the created GitHub repo link. 
* At the AWS CodeCommit Platform: name your repository and choose 'No Secret Key', if your repository is public - which is the case in this example
Back to the notebook instance creation process, you can choose that repo that has been created and proceed with 'Create Notebook Instance'

## Step 3
click on the notebook instance which you had created on the Notebook Instances homepage, and at the Permissions/Encryption tabs, click on the IAM ARN link, and we will need to click on 'Attach Policy', and search for 'AWSCodeCommitPowerUser'. Add that policy to your IAM so that we'll be able to commit our changes to the GitHub repository

## Step 4
Open Jupyter and initialize a conda-python3 instance notebook, of which the code in mnist-pyspark is based on 

## Step 5
Once the codes are up and running, return to the Notebook Instances homepage and click on 'Jupyter Lab'
You'll be able to commit your code to GitHub via JupyterLab. Click on the 'Upload' Icon on the 'Untracked' tab. The notebook will be staged for commit, and then proceed to choose the 'Push Committed Changes' Icon to commit changes to your GitHub repo. You'll be prompted to provide the username and password of your GitHub in order to commit the changes
