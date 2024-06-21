---
layout: page
title: Connect-HVServer
#permalink: /powercli/horizon/vmware.vimautomation.horizonview/connect-hvserver/
hide:
  #- navigation
  - toc
---

This cmdlet establishes a connection to the Horizon API service of the Horizon Connection server specified by the `-Server` parameter. The connect and disconnect operations for a server use a reference counting mechanism. Every server is identified by its connection string which contains a unique server and user name. If there is already an existing connection to the server, a new connection is not established. Instead, the cmdlet returns the object which represents the existing connection. The RefCount property of the object is incremented by one. When a server is disconnected, then its RefCount property is decreased by one. If this number becomes equal to zero, then the server is disconnected.

PowerCLI supports a list of default servers on which the Horizon API service runs. The Horizon API service runs on an instance of the Horizon Connection server. When an operation is performed, if the target servers cannot be determined from the specified parameters, the cmdlet runs against the servers in the default server list. 

The target servers are kept in a global variable called `$DefaultHVServers`. The variable is of an array type and its initial value is an empty array. When you connect to a server, the server is added at the beginning of the array, unless `-NotDefault` parameter is specified. When you disconnect from a server, the server is removed from the `$DefaultHVServers` variable. When all servers are removed from the variable, its value is an empty array.

## Syntax

=== "Credential"

    ```Powershell
    Connect-HVServer    [-Server]  <String> 
                        -Credential  <PSCredential> 
                        [-Domain  <String>] 
                        [-Force] 
                        [-NotDefault] 
                        [CommonParameters] 
    ```
  
=== "Default"

    ```Powershell
    Connect-HVServer    [-Server]  <String>
                        [-Domain  <String>]
                        [-Force]
                        [-NotDefault]
                        [-Password  <SecureString>]
                        [-User  <String>]
                        [CommonParameters]
    ```

=== "SessionSecret"

    ```Powershell
    Connect-HVServer    [-Server]  <String>
                        -SessionId  <String>
                        [-Force]
                        [-NotDefault]
                        [CommonParameters]
    ```

## Parameters

| Required | Parameter Name | Type | Position | Features | Description |
| --- | --- | --- | --- | --- | --- |
| required | Server | String | 1 |  | Specifies the IP or FQDN of the Horizon Connection server on which the Horizon API service runs. |
| required | SessionId | String | named |  | Specifies the ID of an existing Horizon Connection server session that you want to reestablish. |
| optional | Force | SwitchParameter | named |  | Suppresses all user interface prompts during the cmdlet execution such as multiple default servers and invalid certificate action. |
| optional | NotDefault | SwitchParameter | named |  | Specifies that you do not want to save the specified servers as default servers. |

## Output

[VMware.VimAutomation.HorizonView.Types.V1.ViewServer](../../../../horizon-apis/horizon-server/index.md#API-Reference)

## Examples

### Example 1

```Powershell
Connect-HVServer -Server server -User username -Password pass -Domain domain
```

Connects to the Horizon API service that runs on an instance of a Horizon Connection server by using the User, Password, and Domain parameters.

### Example 2

```Powershell
$cs = Connect-HVServer -Server server -Username user -Password pass -Domain domain;
Connect-HVServer -Server server -SessionId $cs.SessionSecret
```

Connects to the Horizon API service that runs on an instance of a Horizon Connection server with an existing session and returns the Horizon API service object. Username is alias to parameter user.

### Example 3

```Powershell
Connect-HVServer -Server server -User username@domain -Password pass
```

Connects to the Horizon API service of a Horizon Connection server by passing the domain as a part of the user name and returns the Horizon API service object.

### Example 4

```Powershell
Connect-HVServer -Server server
```

Connects to the Horizon API service that runs on an instance of a Horizon Connection server. The user, domain, and password parameters are prompted for and read by the PowerCLI user interface. Returns the Horizon API service object.

## Related Commands

### HVServer

[Disconnect-HVServer](../disconnect-hvserver/index.md)
This cmdlet closes the connection to one or more Horizon API services that run on one or more instances of Horizon Connection servers.
