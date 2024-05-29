---
layout: page
title: Disconnect-HVServer
permalink: /powercli/horizon/vmware.vimautomation.horizonview/disconnect-hvserver/
---

This cmdlet disconnects the connection to a Horizon API service that runs on an instance of the Horizon Connection server specified by the `-Server` parameter. When there are no active connections to the server, the server is disconnected and removed from the `$DefaultHVServers` variable. For more information about this variable, see [Connect-HVServer](../connect-hvserver/index.md).

When no server and no user parameter is specified, and if there is only one connected server in the `$DefaultHVServers` variable, this server is disconnected. If there is no connected server or multiple servers, the cmdlet throws a terminating error. This functionality uses the reference counting mechanism. A disconnect decreases the RefCount for that server. For more information about the mechanism, see [Connect-HVServer](../connect-hvserver/index.md).

If `-Force` is specified, the server is disconnected even if there is more than one connection to it.

# Syntax

=== "Default"
  ```
    Disconnect-HVServer [-Force]
                        [-Server  <ViewServer[]>]
                        [CommonParameters]
  ```

## Parameters

| Required | Parameter Name | Type | Position | Features | Description |
| --- | --- | --- | --- | --- | --- |
| optional | Force | SwitchParameter | named |  | Specifies that you want to remove all existing connections to the specified servers. |
| optional | Server | ViewServer[] | named | pipeline | Specifies the Horizon API service that runs on an instance of a Horizon Connection server that you want to disconnect from. |

## Output

[VMware.VimAutomation.HorizonView.Types.V1.ViewServer](../../../../apis/horizon-server/index.md#API-Reference)

## Examples
### Example 1
`$HVServer = Connect-HVServer -Server server; Disconnect-HVServer -server $HVServer`
Disconnects the connection to the specified Horizon API service that runs on an instance of a Horizon Connection server.

### Example 2
`$HVServer = Connect-HVServer -Server server; Disconnect-HVServer -Force *`
Disconnects all connected Horizon API services that run on instances of Horizon Connection servers.

## Related Commands
### HVServer
[Connect-HVServer](../connect-hvserver/index.md)  
This cmdlet establishes a connection to the Horizon API service that runs on an instance of the Horizon Connection server.