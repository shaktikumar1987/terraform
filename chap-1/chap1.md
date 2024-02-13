## How to Install The Terraform on Ubuntu ##
# 1. Run the below command with root user
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
# 2. install az cli
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-linux?pivots=apt
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
## AZ Login ##
it will provide yo the device code and you can connect with that or you can see connection method 
https://registry.terraform.io/providers/hashicorp/azurerm/latest/docs/guides/azure_cli

# how to use secret
# a. Create appliaction in azure and create secret and fill the below information
{
  "appId": "XXXXXX",
  "displayName": "Terraform",
  "name": "Add an Application ID URI",
  "password": "XXXXXXX",
  "tenant": "XXXXXXXXX"
}

appId is the client_id defined above.
password is the client_secret defined above.
tenant is the tenant_id defined above
#