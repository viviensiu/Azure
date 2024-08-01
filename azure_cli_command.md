## Azure CLI commands
- Always begin with ```az <command>``` (except when in interactive mode).

**Commands**
* ```upgrade```: upgrades Azure version.
* ```interactive```: enters interactive mode that provides autocompletion, command descriptions, and even examples. Note that you can key in commands directly without ```az``` in this mode.
* ```exit```: Leaves interactive mode.

**Example to create a VM and install Nginx on VM**
* Creates VM: ```vm create --resource-group <group name> --name <vm name> --public-ip-sku Standard --image <img name> --admin-username <username> --generate-ssh-keys```.
* Configure Nginx on your VM: ```vm extension set --resource-group "learn-02c66e66-4e63-4e4d-87a6-eca85d7ebe33" --vm-name my-vm --name customScript --publisher Microsoft.Azure.Extensions --version 2.1 --settings '{"fileUris":["https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh"]}' --protected-settings '{"commandToExecute": "./configure-nginx.sh"}'```
* This bash script [configure-nginx.sh](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-welcome-to-azure/master/configure-nginx.sh):
    - Runs apt-get update to download the latest package information from the internet. This step helps ensure that the next command can locate the latest version of the Nginx package.
    - Installs Nginx.
    - Sets the home page, /var/www/html/index.html, to print a welcome message that includes your VM's host name.