---
layout: page
title: Horizon PowerCLI
hide:
  #- navigation
  - toc
---

The Omnissa.VimAutomation.HorizonView powershell module provides Connect/Disconnect cmdlets for View API service.

The [Omnissa.Horizon.Helper](https://github.com/euc-oss/euc-samples/tree/main/Horizon-Samples/Omnissa.Horizon.Helper) Powershell Module extends the capabilities provided by the `Omnissa.VimAutomation.HorizonView` module. It can Add, create New, Get, Set, Start and Remove Global, Farm and Pool settings.

## Using Horizon Powercli

1. Import HorizonView module by running: `Import-Module Omnissa.VimAutomation.HorizonView.`
2. Import "Omnissa.Horizon.Helper" module by running: `Import-Module -Name Omnissa.Horizon.Helper`. Alternatively run `Get-Module -ListAvailable 'Omnissa.Horizon.Helper' | Import-Module`.
3. Run `Get-Command -Module 'Omnissa.Horizon.Helper'` to list all available functions.

## Getting Started with Omnissa Horizon cmdlets

Cmdlets are usually implemented around resource operations. The four basic operations are CREATE, READ, UPDATE and DELETE. This set of operations is known as CRUD. Most of the cmdlets support CRUD which are respectively cmdlets that start with the New/Get/Set/Remove cmdlet verbs but they also may have additional operations.

**Omnissa.VimAutomation.HorizonView** module provides two commandlets:

1. [`Connect-HVServer`](connect-hvserver/index.md) This cmdlet establishes a connection to the Horizon API service that runs on an instance of the Horizon Connection server.
2. [`Disconnect-HVServer`](disconnect-hvserver/index.md) This cmdlet closes the connection to one or more Horizon API services that run on one or more instances of Horizon Connection servers.

**Omnissa.Horizon.Helper Powershell Module** module provides many additional commandlets which are linked in the menu to the left.

## Example Scripts

### Example script to connect ViewAPI service

```
Import-Module Omnissa.VimAutomation.HorizonView

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
