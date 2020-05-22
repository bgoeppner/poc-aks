# How to configure your environment

## Vorbereiten
Die folgenden Befehle in [Azure Cloud Shell](https://docs.microsoft.com/de-de/powershell/azure/get-started-azureps?view=azps-4.1.0) ausführen. Falls nicht vorhanden, folgende Befehle in Powershell ausführen:
```
Install-Module -Name Az -AllowClobber -Scope CurrentUser
Connect-AzAccount
```
Ggf. muss noch die Subscription gesetzt werden.


## Resourcengruppe in Azure anlegen 
```
$rg = "poc-aks"
$loc = "westeurope"

New-AzResourceGroup -Name $rg -Location $loc
New-AzResourceGroupDeployment -ResourceGroupName $rg `
    -TemplateFile template.json `
    -resourceGroup_name $rg `
    -containerRegistry_name "45sdf2" `
    -managedCluster_name "45sdf2"
```