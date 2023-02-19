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


### Next step would be to productionalize the model using MLPOps pipelines using a multi account deploymet process to Dev, QA and PROD. Below are the standard steps follows for productionalizing a model at scale

Pre-requisites for multi account deployment using MLOps process
1. Data Scientists will upload the source code, yaml files, score.py, testing scripts, environment details
2. ML Engineers to create the template files for ML pipelines and confifurations required for training jobs like compute type
3. DevOps engineers will create the 



