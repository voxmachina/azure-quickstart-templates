# Ansible Tower on Azure 
## Solution Overview 
This push to pilot template deploys an Ansible Tower Solution on Azure Virtual Machines running RHEL 7.2. Template will build everything starting from Azure Infrastructure components to Ansible Tower and Clients installation, configuration etc. To start with, this template will deploy one Ansible tower server vm and 2 clients.

Ansible Tower by Red Hat helps you scale IT automation, manage complex deployments and speed productivity. Centralize and control your IT infrastructure with a visual dashboard, role-based access control, job scheduling and graphical inventory management.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fansible-tower-rhel%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.png"/>
</a>
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fansible-tower-rhel%2Fazuredeploy.json" target="_blank">
<img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.png"/>
</a> 


Once deployment finishes, you will able to directly access fully configured tower GUI and connect with Ansible Clients. 

##Deployment Solution Architecture 

This template will deploy: 

-   3 storage accounts
-	One Virtual Network with two subnets
-	Two Network Security Groups, one for each subnet
-	3 Public IP’s, one for tower and 2 for clients 
-	Virtual Machines Availability set for tower and client vms.
-	One Ansible Tower Virtual Machine (RHEL 7.2)
-	Two Ansible Client Virtual Machine (RHEL 7.2)
-	Installation and configuration of Ansible Tower Server and Clients


![Deployment Solution Architecture](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/ansible-tower-rhel/images/ansible-architecture.png?raw=true)

##Licenses and Costs 

This uses RHEL 7.2 image which is a PAY AS YOU GO image and doesn't require the user to license it, it will be licensed automatically after the instance is launched first time and user will be charged hourly in addition to Microsoft's Linux VM rates.  Click [here](https://azure.microsoft.com/en-gb/pricing/details/virtual-machines/linux/#red-hat) for pricing details.

##Prerequisites 

- Azure Subscription with specified payment method (RHEL 7.2 is a marketplace product and requires payment method to be specified in Azure Subscription)
- Ansible Tower License( You can get a free trial license from [here](https://www.ansible.com/license) )

##Deployment Steps  

Build your Ansible Tower environment on Azure in a few simple steps: 

- Launch the Template by clicking on Deploy to Azure button.  
- Fill in all the required parameter values. Accept the terms and condition and click Purchase. The deployment takes about 20 minutes. 
- Access the deployment job once it is successful. In deployment job output you will find the Public IP Address of client and tower VMs so you can easily connect to the VMs. Make a note of the public of Tower VM.Alternatively you can get public ip address of VM from Overview Blade in VM settings.
- Access Ansible GUI with the public ip of tower vm noted in above step by opening http://publicip
- Login with username as ‘admin’ and password specified in parameters during deployment. 
- Request a trial Ansible license or provide your existing Ansible license file. You should get license file within 3-5 minutes on email after requesting a trial.
- You will now have access to working Ansible Tower Server. 
- Follow the post deployment configuration document [here](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/ansible-tower-rhel/images/ansible-tower-rhel-postdeployment-configuration-guide.pdf) to learn about further configuration. 

##Support 

For any support related questions or customization requirements, please contact info@spektrasystems.com



