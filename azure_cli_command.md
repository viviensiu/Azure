## Azure CLI commands
- Always begin with ```az <command>``` (except when in interactive mode).

**Commands**
* ```az upgrade```: upgrades Azure version.
* ```az interactive```: enters interactive mode that provides autocompletion, command descriptions, and even examples. Note that you can key in commands directly without ```az``` in this mode.
* ```az exit```: Leaves interactive mode.

**Example to create a VM and install Nginx on VM**
* Creates VM: ```az vm create --resource-group <group name> --name <vm name> --public-ip-sku Standard --image <img name> --admin-username <username> --generate-ssh-keys```.
* Configure Nginx on your VM: ```az vm extension set --resource-group <group name> --vm-name <vm name> --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'```
* This bash script [configure-nginx.sh](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh):
    - Runs apt-get update to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
    - Installs Nginx.
    - Sets the home page, /var/www/html/index.html, to print a welcome message that includes your VM's host name.

**Example to create a network security group that allows inbound HTTP access on port 80**
* Get your VM's IP address ```az vm list-ip-addresses``` and store the result as a Bash variable: ```IPADDRESS="$(az vm list-ip-addresses --resource-group <group name> --name <vm name> --query "[].virtualMachine.network.publicIpAddresses[*].ipAddress" --output tsv)"```.
* Run ```az network nsg list``` command to list the network security groups that are associated with your VM: ```az network nsg list --resource-group <group name> --query '[].name' --output tsv```.
* Run ```az network nsg rule list``` command to list the rules associated with the NSG named my-vmNSG: ```az network nsg rule list --resource-group <group name> --nsg-name <NSG name> --query '[].{Name:name, Priority:priority, Port:destinationPortRange, Access:access}' --output table```. You should only one rule with port 22.
* Run ```az network nsg rule create``` command to create a rule called allow-http that allows inbound access on port 80: ```az network nsg rule create --resource-group "learn-bed537ae-4e0e-449a-8cf5-35e83bdd3356" --nsg-name my-vmNSG --name allow-http --protocol tcp --priority 100 --destination-port-range 80 --access Allow```.
* Confirm port 80 is created by rerunning the ```az network nsg rule list``` command above.

