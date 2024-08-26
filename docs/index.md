---
layout: page
title: Horizon PowerCLI
hide:
  #- navigation
  - toc
---

The [VMware.VimAutomation.HorizonView](https://www.powershellgallery.com/packages/VMware.VimAutomation.HorizonView/) powershell module provides Connect/Disconnect cmdlets for View API service.

The [VMware.Hv.Helper](https://github.com/euc-oss/euc-samples/tree/Horizon-Samples/VMware.Hv.Helper) Powershell Module extends the capabilities provided by the `VMware.VimAutomation.HorizonView` module. It can Add, create New, Get, Set, Start and Remove Global, Farm and Pool settings.

## Installation

Installation instructions can be found within the module listing in the [Powershell Gallery](https://www.powershellgallery.com/).

1. Import HorizonView module by running: `Import-Module VMware.VimAutomation.HorizonView.`
2. Import "VMware.Hv.Helper" module by running: `Import-Module -Name VMware.Hv.Helper`. Alternatively run `Get-Module -ListAvailable 'VMware.Hv.Helper' | Import-Module`.
3. Run `Get-Command -Module 'VMware.Hv.Helper'` to list all available functions.

## Prerequisites

1. This module only works for Horizon product E.g. Horizon 7.0.2 and later.
2. Install the latest version of Powershell, PowerCLI(6.5) or (later version via psgallery).

## Getting Started with VMware Horizon cmdlets

Cmdlets are usually implemented around resource operations. The four basic operations are CREATE, READ, UPDATE and DELETE. This set of operations is known as CRUD. Most of the cmdlets support CRUD which are respectively cmdlets that start with the New/Get/Set/Remove cmdlet verbs but they also may have additional operations.

**VMware.VimAutomation.HorizonView** module provides two commandlets:

1. [`Connect-HVServer`](connect-hvserver/index.md) This cmdlet establishes a connection to the Horizon API service that runs on an instance of the Horizon Connection server.
2. [`Disconnect-HVServer`](disconnect-hvserver/index.md) This cmdlet closes the connection to one or more Horizon API services that run on one or more instances of Horizon Connection servers.

**VMware.Hv.Helper Powershell Module** module provides many additional commandlets which are linked in the menu to the left.
<!-- 
* [Add-HVDesktop.md](VMware.Hv.Helper/Add-HVDesktop.md)
* [Add-HVRDSServer.md](VMware.Hv.Helper/Add-HVRDSServer.md)
* [Clear-HVEventDatabase.md](VMware.Hv.Helper/Clear-HVEventDatabase.md)
* [Connect-HVEvent.md](VMware.Hv.Helper/Connect-HVEvent.md)
* [Disconnect-HVEvent.md](VMware.Hv.Helper/Disconnect-HVEvent.md)
* [Get-HVApplication.md](VMware.Hv.Helper/Get-HVApplication.md)
* [Get-HVBaseImageVM.md](VMware.Hv.Helper/Get-HVBaseImageVM.md)
* [Get-HVEntitlement.md](VMware.Hv.Helper/Get-HVEntitlement.md)
* [Get-HVEvent.md](VMware.Hv.Helper/Get-HVEvent.md)
* [Get-HVEventDatabase.md](VMware.Hv.Helper/Get-HVEventDatabase.md)
* [Get-HVFarm.md](VMware.Hv.Helper/Get-HVFarm.md)
* [Get-HVFarmSummary.md](VMware.Hv.Helper/Get-HVFarmSummary.md)
* [Get-HVGlobalEntitlement.md](VMware.Hv.Helper/Get-HVGlobalEntitlement.md)
* [Get-HVGlobalSession.md](VMware.Hv.Helper/Get-HVGlobalSession.md)
* [Get-HVGlobalSettings.md](VMware.Hv.Helper/Get-HVGlobalSettings.md)
* [Get-HVHealth.md](VMware.Hv.Helper/Get-HVHealth.md)
* [Get-HVHomeSite.md](VMware.Hv.Helper/Get-HVHomeSite.md)
* [Get-HVInternalName.md](VMware.Hv.Helper/Get-HVInternalName.md)
* [Get-HVLocalSession.md](VMware.Hv.Helper/Get-HVLocalSession.md)
* [Get-HVMachine.md](VMware.Hv.Helper/Get-HVMachine.md)
* [Get-HVMachineSummary.md](VMware.Hv.Helper/Get-HVMachineSummary.md)
* [Get-HVPodFederation.md](VMware.Hv.Helper/Get-HVPodFederation.md)
* [Get-HVPool.md](VMware.Hv.Helper/Get-HVPool.md)
* [Get-HVPoolSpec.md](VMware.Hv.Helper/Get-HVPoolSpec.md)
* [Get-HVPoolSummary.md](VMware.Hv.Helper/Get-HVPoolSummary.md)
* [Get-HVPreInstalledApplication.md](VMware.Hv.Helper/Get-HVPreInstalledApplication.md)
* [Get-HVQueryFilter.md](VMware.Hv.Helper/Get-HVQueryFilter.md)
* [Get-HVQueryResult.md](VMware.Hv.Helper/Get-HVQueryResult.md)
* [Get-HVResourceStructure.md](VMware.Hv.Helper/Get-HVResourceStructure.md)
* [Get-HVSite.md](VMware.Hv.Helper/Get-HVSite.md)
* [Get-HVlicense.md](VMware.Hv.Helper/Get-HVlicense.md)
* [Get-HVvCenterServer.md](VMware.Hv.Helper/Get-HVvCenterServer.md)
* [Get-HVvCenterServerHealth.md](VMware.Hv.Helper/Get-HVvCenterServerHealth.md)
* [New-HVEntitlement.md](VMware.Hv.Helper/New-HVEntitlement.md)
* [New-HVFarm.md](VMware.Hv.Helper/New-HVFarm.md)
* [New-HVGlobalEntitlement.md](VMware.Hv.Helper/New-HVGlobalEntitlement.md)
* [New-HVHomeSite.md](VMware.Hv.Helper/New-HVHomeSite.md)
* [New-HVManualApplication.md](VMware.Hv.Helper/New-HVManualApplication.md)
* [New-HVPodFederation.md](VMware.Hv.Helper/New-HVPodFederation.md)
* [New-HVPool.md](VMware.Hv.Helper/New-HVPool.md)
* [New-HVPreInstalledApplication.md](VMware.Hv.Helper/New-HVPreInstalledApplication.md)
* [New-HVSite.md](VMware.Hv.Helper/New-HVSite.md)
* [Register-HVPod.md](VMware.Hv.Helper/Register-HVPod.md)
* [Remove-HVApplication.md](VMware.Hv.Helper/Remove-HVApplication.md)
* [Remove-HVApplicationIcon.md](VMware.Hv.Helper/Remove-HVApplicationIcon.md)
* [Remove-HVEntitlement.md](VMware.Hv.Helper/Remove-HVEntitlement.md)
* [Remove-HVFarm.md](VMware.Hv.Helper/Remove-HVFarm.md)
* [Remove-HVGlobalEntitlement.md](VMware.Hv.Helper/Remove-HVGlobalEntitlement.md)
* [Remove-HVMachine.md](VMware.Hv.Helper/Remove-HVMachine.md)
* [Remove-HVPodFederation.md](VMware.Hv.Helper/Remove-HVPodFederation.md)
* [Remove-HVPool.md](VMware.Hv.Helper/Remove-HVPool.md)
* [Remove-HVSite.md](VMware.Hv.Helper/Remove-HVSite.md)
* [Reset-HVMachine.md](VMware.Hv.Helper/Reset-HVMachine.md)
* [Set-HVApplication.md](VMware.Hv.Helper/Set-HVApplication.md)
* [Set-HVApplicationIcon.md](VMware.Hv.Helper/Set-HVApplicationIcon.md)
* [Set-HVEventDatabase.md](VMware.Hv.Helper/Set-HVEventDatabase.md)
* [Set-HVFarm.md](VMware.Hv.Helper/Set-HVFarm.md)
* [Set-HVGlobalEntitlement.md](VMware.Hv.Helper/Set-HVGlobalEntitlement.md)
* [Set-HVGlobalSettings.md](VMware.Hv.Helper/Set-HVGlobalSettings.md)
* [Set-HVInstantCloneMaintenance.md](VMware.Hv.Helper/Set-HVInstantCloneMaintenance.md)
* [Set-HVMachine.md](VMware.Hv.Helper/Set-HVMachine.md)
* [Set-HVPodFederation.md](VMware.Hv.Helper/Set-HVPodFederation.md)
* [Set-HVPool.md](VMware.Hv.Helper/Set-HVPool.md)
* [Set-HVSite.md](VMware.Hv.Helper/Set-HVSite.md)
* [Set-HVlicense.md](VMware.Hv.Helper/Set-HVlicense.md)
* [Start-HVFarm.md](VMware.Hv.Helper/Start-HVFarm.md)
* [Start-HVPool.md](VMware.Hv.Helper/Start-HVPool.md)
* [Unregister-HVPod.md](VMware.Hv.Helper/Unregister-HVPod.md) -->

## Example Scripts

### Example script to connect ViewAPI service

```
Import-Module VMware.VimAutomation.HorizonView

# Connection to view API service
$hvServer = Connect-HVServer -server <connection server IP/FQDN>
$hvServices = $hvserver.ExtensionData

# List Connection Servers
$csList = $hvServices.ConnectionServer.ConnectionServer_List()
```

### Use advanced functions of this module

```
New-HVPool -spec 'path to InstantClone.json file'
```
