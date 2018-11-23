# Dockerizing Applications with Azure Container Registry

## Azure Container Registry (ACR)

We will use Azure COntainer Registry to build our containers from Dockerfiles and also host our images to run in AKS

### Create Azure Container Registry instance

1. In the browser, sign in to the Azure portal at https://portal.azure.com. Your Azure login ID will look something like `odl_user_9294@gbbossteamoutlook.onmicrosoft.com`
2. Click "Create a resource" and select "Container Registry"
3. Provide a name for your registry (this must be unique)
4. Use the existing Resource Group
5. Enable the Admin user
6. Use the 'Standard' SKU (default)

    > The Standard registry offers the same capabilities as Basic, but with increased storage limits and image throughput. Standard registries should satisfy the needs of most production scenarios.

For the first container, we will be creating a Dockerfile from scratch. For the other containers, the Dockerfiles are provided.

### Web Container

1. Create a container image for the node.js Web app

    From the terminal session: 

    ```
    cd ~/blackbelt-aks-hackfest/app/web
    
    # Set environment variable for ACR Name
    ACR_NAME=<registry-name>
    az acr build --registry $ACR_NAME --image azureworkshop/rating-web:v1 .
    
    ```
    1. Return to the Azure Portal in your browser and validate that the image appears in your Container Registry under the "Repositories" area.
    2. Under tags, you will see "v1" listed.

### API Container

In this step, the Dockerfile has been created for you. 

1. Create a container image for the node.js API app

    ```
    cd ~/blackbelt-aks-hackfest/app/api

   az acr build --registry $ACR_NAME --image azureworkshop/rating-api:v1 .
    
    ```
    1. Return to the Azure Portal in your browser and validate that the image appears in your Container Registry under the "Repositories" area.
    2. Under tags, you will see "v1" listed.


### MongoDB Container

1. Create a MongoDB image with data files

    ```
    cd ~/blackbelt-aks-hackfest/app/db

    az acr build --registry $ACR_NAME --image azureworkshop/rating-db:v1 .
    
    ```
    1. Return to the Azure Portal in your browser and validate that the image appears in your Container Registry under the "Repositories" area.
    2. Under tags, you will see "v1" listed.



