This will create an Azure Availability Set.  
To tailor the deployment, create a new Parameters File.  
Run the following Powershell Cmdlet in Azure Portal using the cloud shell.  
If you need to provide a customised parameters file, update the file location referenced in $ParameterURI.  


$ParameterURI = "https://raw.githubusercontent.com/EnfoPaul/ARM-Templates/main/AvailabilitySet/defaultParams.json"

$TemplateURI = "https://raw.githubusercontent.com/EnfoPaul/ARM-Templates/main/AvailabilitySet/DeployAVSet.json"
New-AzResourceGroupDeployment -Name remoteTemplateDeployment -ResourceGroupName AZ-Web -TemplateUri $TemplateURI -TemplateParameterUri $ParameterURI
