# MNIST_AZURE_ML

#### Use case: Train and deploy an image classification model in Azure Machine Learning using MNIST dataset

As part of the take home assignment, i have tried to implment the code using Azure ML. 

### For the experimentation phase, I have done the below steps to deploy the model as a real time endpoint. 
1. Download a dataset and look at the data
2. Train an image classification model and log metrics using MLflow
3. Check the Model performance matrix
4. Deploy the model to a real time endpoint
5. Test the model using a web request

### How to use the code?
1. Clone or Upload the MNIST_AZURE folder in AzureMachine Learning Studio Notebooks
2. Run the notebook file
3. Get the scoring url from the real time endpoint created after the successful run
5. You can use a python code or third party API like POSTMAN to invoke the endpoint using the scoring url and get the prediction results

-------------------------------------------------------------------------------------------------------------------------------------------------------


#####  Next step would be to productionalize the model using MLOps pipelines using a multi account deploymet process to QA and PROD. Below are the standard steps for productionalizing a model at scale

Pre-requisites for multi account deployment using MLOps process
1. Create a Azure DevOps project 
2. Data Scientists will upload the source code, yaml files, score.py, testing scripts, environment details in Code Repo
3. ML Engineers to create the template files for ML pipelines and confifurations required for training jobs like compute type and upload to Code Repo
4. DevOps engineers will create the required configuration files and scripts to run the ML pipelines and IaC pipelines and upload to Code Repo

Deployment to QA
1. Create a Iac pipeline in the Azure DevOps project: Create the azure resources like resource group, ML workspace, compute instance, storage accounts etc using Terraform scripts in QA environment
2. Create a Continuous Integration Pipeline in Azure DevOps project and add the scripts for the below tasks for automated run in QA environment
    a. Register the dataset to ML workspace if required
    b. Run Code Testing scripts
    c. Train and register the model
    d. Baseline the date quality
    f. Baseline the model quality
3. Create a Continuous Deployment Pipeline in Azure DevOps project and add the scripts for the below tasks for automated run in QA environment
    a. Deploy the model to an online endpoint
    b. Smoke testing 
Based on the succesful testing in QA environment, we can start the automated deployment to PROD
4. Create a Iac pipeline in the Azure DevOps project: Create the azure resources like resource group, ML workspace, compute instance, storage accounts etc using Terraform scripts in PROD environment
5. Create a Continuous Deployment Pipeline in Azure DevOps project and add the scripts for the below tasks for automated run in QA environment
    a. Download the required version of model from model registry in QA
    b. Deploy the model to an online endpoint
    e. Smoke testing
 6. Create a Monitoring pipeline to monitoring to review the data drift or model drift (Based on ground truth availabilty) and system performance matrices to alert users in case of any issues
Trigger the CI pipeline incase retraining is required with the new dataset or with the new code





