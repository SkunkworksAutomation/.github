# Skunkworks Automation
This is an unofficial Dell github focused on data protection automation.
We have a ton of additional automation content coming but we want to ensure we post meaningful, relevant, and functional examples to address the most common data protection use cases.
We'll be working over the next few weeks to align with the conventions defined below for each product covered.

# Notes:
I have removed the Ansible examples for now until I can get some conventions in place. They will be back soon!

# Authors
Cliff Rodriguez
  * [Dell Technoligies](https://www.dell.com/en-us)
  * [LinkedIn](https://www.linkedin.com/in/cliff-rodriguez-6673422b/)
# Platforms
* PowerShell7
  * [CMDLET Guidelines](https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/strongly-encouraged-development-guidelines?view=powershell-7.3)
  * CMDLET names are in lower case
  * CMDLET names begin with a PowerShell [approved verb](https://learn.microsoft.com/en-us/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands?view=powershell-7.3)
  * CMDLET nouns are prefixed with two characters to avoid any naming convention collisions
    * ap = APEX
    * av = Avamar
    * dd = PowerProtect Data Domain
    * dm = PowerProtect Data Manager
    * dp = Data Protection Advisor
    * nw = Networker
    * rp = RP4VM
  * CMDLET variables are in pascal case
  * CMDLET bindings must be used outside of the following global variables
    * $global:ApiVersion
    * $global:AuthObject
    * $global:Port
  * CMDLET help must be defined
    * List module functions
      * PS> Import-Module .\dell.ppdm.psm1 -Force
      * PS> Get-Command -Module dell.ppdm
    * List cmdlet help after module is imported (basic, detailed, verbose w/ examples)
      * PS> {cmdlet-name} -?
      * PS> Get-Help -Name {cmdlet-name} -Detailed
      * PS> Get-Help -Name {cmdlet-name} -Full
      * PS> Get-Help -Name {cmdlet-name} -Examples
# Documentation
* PowerShell 7.[latest](https://learn.microsoft.com/en-us/powershell)
