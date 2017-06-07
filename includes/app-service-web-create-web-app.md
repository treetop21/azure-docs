## Create a web app

Create a [web app](../articles/app-service-web/app-service-web-overview.md) in the `myAppServicePlan` App Service plan with the [az appservice web create](/cli/azure/appservice/web#create) command. Note: az appservice web create is being depricated, instead use az webapp create.

The web app provides a hosting space for your code and provides a URL to view the deployed app.

In the following command, replace *\<app_name>* with a unique name. If `<app_name>` is not unique, you get the error message "Website with given name <app_name> already exists." The default URL of the web app is `https://<app_name>.azurewebsites.net`. 

```azurecli-interactive
az appservice web create --name <app_name> --resource-group myResourceGroup --plan myAppServicePlan
```

When the web app has been created, the Azure CLI shows information similar to the following example:

```json
{
  "availabilityState": "Normal",
  "clientAffinityEnabled": true,
  "clientCertEnabled": false,
  "cloningInfo": null,
  "containerSize": 0,
  "dailyMemoryTimeQuota": 0,
  "defaultHostName": "<app_name>.azurewebsites.net",
  "enabled": true,
  "enabledHostNames": [
    "<app_name>.azurewebsites.net",
    "<app_name>.scm.azurewebsites.net"
  ],
  "gatewaySiteName": null,
  "hostNameSslStates": [
    {
      "hostType": "Standard",
      "name": "<app_name>.azurewebsites.net",
      "sslState": "Disabled",
      "thumbprint": null,
      "toUpdate": null,
      "virtualIp": null
    }
    < JSON data removed for brevity. >
}
```

Browse to the site to see your newly created web app.

```bash
http://<app_name>.azurewebsites.net
```
