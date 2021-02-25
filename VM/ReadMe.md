Azure ARM Template to deploy multiple Windows Server 2016 VMs

Usage:
Modify the parameter.json template to suit your requirements
Run the following powershell code from Azure console, updating the $RGName with the name of the resource group where the VMs should be deployed in your Azure tenant.

$ParameterURI = "https://raw.githubusercontent.com/EnfoPaul/ARM-Templates/VM/VMParameters.json"
$TemplateURI = "https://raw.githubusercontent.com/EnfoPaul/ARM-Templates//VM/CreateVMs.json" 
$RGName ="AZ-Web"

New-AzResourceGroupDeployment -Name DeployAVSetVMs -ResourceGroupName $RGName -TemplateUri $TemplateURI -TemplateParameterUri $ParameterURI
