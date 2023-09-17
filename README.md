# azure_flask_deployment
## HHA 504 Assignment #2 

# Azure Flask Deployment
Steps taken to deploy a Flask application to Azure App Service. The deployment process was through the Cloud Shell terminal and involved mulitple commands using the Azure CLI. 

## Flask - Google Cloud Shell 
- Week 2 --> flaskapp_0 and classwork were used to initiate a new flask application. It included: 
    - Templates folder with 'about.html' , 'base.html' , and 'random.html' 
    - 'app.py' file 
    - 'README.md' and 'requirements.txt'


## Deployment Steps

## Step 1: Azure Login

Login to Azure was initiated using the command:

```
az login --use-device-code
```

## Step 2: Subscription

The list of available subscriptions was retrieved using the command:

```sh
az account list --output table
```

From the table, the  subscription id code was copied and pasted into the following code:

```sh
az account set --subscription "subscription code "
```

## Step 3: Creating Resource Group

On the Azure web page, a new resource group named `Stephen-504` was created.

## Step 5: Deployment

The following command was used for initial deployment:

```sh 
az webapp up --resource-group Stephen-504 --name StephenApp --runtime "PYTHON:3.9" --sku B1
``` 

## Final Result

The application was successfully deployed and is accessible via the following URL:

[**Stephen-504-Flask Application**](http://stephenapp.azurewebsites.net)

`