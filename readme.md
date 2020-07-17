# arm-vm-customregion

A quick ARM template to demonstrate the use of autologon to set system configuration prior to first user login. Based off the [101-vm-simple-windows Quickstart Template](https://github.com/Azure/azure-quickstart-templates/tree/master/101-vm-simple-windows)

## Usage

NB: Deliberately creates the machine in ***westus*** region

```sh
az group create --name demo-customregion -l westus
az deployment group create -g demo-customregion --template-file azuredeploy.json --parameters azuredeploy.parameters.json --parameters adminUsername=azureuser --parameters adminPassword=YOURADMINPASSWORD --parameters dnsLabelPrefix=sp20200701
```

## Author

Stuart Preston
