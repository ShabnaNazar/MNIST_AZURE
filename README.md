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
3. A REST API will be created during the real time endpoint deployment
4. Get the scoring url from the real time endpoint
5. You can use a python code or third party API like POSTMAN to invoke the endpoint and get the prediction results

### Next step would be to productionalize the model using MLPOps pipelines using a multi account deploymet process to Dev, QA and PROD



