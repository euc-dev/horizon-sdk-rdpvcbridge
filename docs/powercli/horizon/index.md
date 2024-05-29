---
layout: page
title: Horizon PowerCLI
permalink: /powercli/horizon/
---

The [VMware.VimAutomation.HorizonView](https://www.powershellgallery.com/packages/VMware.VimAutomation.HorizonView/) powershell module provides Connect/Disconnect cmdlets for View API service.

## Installation
Installation instructions can be found within the module listing in the Powershell Gallery at [](https://www.powershellgallery.com/packages/VMware.VimAutomation.HorizonView).

## Getting Started with VMware Horizon cmdlets
Cmdlets are usually implemented around resource operations. The four basic operations are CREATE, READ, UPDATE and DELETE. This set of operations is known as CRUD. Most of the cmdlets support CRUD which are respectively cmdlets that start with the New/Get/Set/Remove cmdlet verbs but they also may have additional operations.

**VMware.VimAutomation.HorizonView** module provides two commandlets:
1. [`Connect-HVServer`](./vmware.vimautomation.horizonview/commands/connect-hvserver/index.md)	This cmdlet establishes a connection to the Horizon API service that runs on an instance of the Horizon Connection server.
2. [`Disconnect-HVServer`](./vmware.vimautomation.horizonview/commands/disconnect-hvserver/index.md)	This cmdlet closes the connection to one or more Horizon API services that run on one or more instances of Horizon Connection servers.
