# SET on a Azure VM

# Prerequisite 
```
git clone https://github.com/derdanu/azure-set.git
cd azure-set
```
## Create a single Azure VM using CLI and the cloudinit file 
```
export GROUP=set
az group create --name $GROUP --location westeurope
az vm create \
    --resource-group $GROUP \
    --name set --image UbuntuLTS \
    --admin-username azureuser \
    --admin-password Test123#123# \
    --nsg ""  \
    --custom-data cloud-init.txt
```
