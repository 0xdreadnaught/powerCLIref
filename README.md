# powerCLIref
Misc powerCLI notes

## Install PowerCLI
`Install-Module -Name VMware.PowerCLI`

## PShell Execution Policy
`Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted -Force`

## Ignore PowerCLI Certificate Error
`Set-PowerCLIConfiguration -InvalidCertificateAction Ignore`

## Connect to VCSA
`Connect-VIServer <VCSA address> -User <user> -Password '<pass>'`
*single quotes will escape characters for password

## Change VM RAM/CPU
`Get-VM -Name <VM name> | Stop-VM -Confirm:$false | Set-VM -MemoryGB <#> -Confirm:$false | Set-VM -NumCpu <#> -Confirm:$false | Start-VM`
  
## Get VM Creation Dates
`(get-vm).ExtensionData.Config.createDate`

