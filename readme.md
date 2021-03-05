# Reading messages from Azure event grid and sending message to MS Teams

Data loads and moniroting needs proactive and timely monitoring. Archiving this it is need to follow up on loads and any fails and errors. This logic app enable you to follow event grid messages that are sent by [ADE](https://www.solita.fi/en/agiledataengine/).

## Requierments

Azure account 
Altleas one ADE environment in Azure
Possibility to create resources 
Resource group
Logic app
Created eventgrid connection(created before hand)


## How to deploy 

Azure Cli installed for this or you can deploy the ARM template from Azure portal as well.


Chaneg the parameters file based on your needs

```


az group create --name rg-logic-app-d --location westeurope

az deployment group create \
  --name monitoring-ade-d \
  --resource-group rg-logic-app-d  \
  --template-file azuredeloy.json\
  --parameters azuredeploy.parameters.json


```

```
-> go azure portal and see if the logic app is there 

```



## Contributing

Feedback and everything else is always welcome. 

Some Design work would be nice 

Initial work:

Kaarel Kõrvemaa 
