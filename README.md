# Azure Functions Python sample for CosmosDB

This project is a small extension of our quickstart: https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-first-azure-function-azure-cli?tabs=bash%2Cbrowser&pivots=programming-language-python

### Pre-reqs

1. Ensure you have the [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest) on your machine (`az`) and logged in with your subscription `az login`.
2. Ensure you have the [Azure Functions core tools](https://github.com/Azure/azure-functions-core-tools#azure-functions-core-tools) (`func`) on your machine.  This is used for project creation, debugging, and deploying.

### How to start

1. Create a virtual environment
    - Windows: `py -m venv env ; env\Scripts\Activate.ps1 ; pip install -r requirements.txt`
    - Linux: `python3 -m venv env && source env\bin\activate && pip install -r requirements.txt`
2. Copy the connection string for your CosmosDB account and paste it into the value in `local.settings.json`
3. Update the metadata in `/CosmosTrigger/function.json` with the name of your database and collection for CosmosDB
4. Copy the connection string for an Azure Storage account and paste it into the value in `local.settings.json`
5. Run the app locally with `func start`, or open in VS Code with the "Azure Functions" extension and debug.

### How to deploy

Follow the [instructions here](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-first-azure-function-azure-cli?tabs=bash%2Cbrowser&pivots=programming-language-python#create-supporting-azure-resources-for-your-function) to deploy.  Your app should have 3 functions, `HttpExample`, `CosmosTrigger`, and `FlaskExample`