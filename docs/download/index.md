---
layout: page
title: Download
hide:
  #- navigation
  - toc
---

Omnissa provides this Powershell Module (the “Software”) to you subject to the [Omnissa General Terms](https://www.omnissa.com/general-terms/). By downloading, installing, or using the Software, you agree to be bound by the terms. If you disagree with any of the terms, then do not use the Software.

For additional information, please visit the [Omnissa Legal Center](https://www.omnissa.com/legal-center/).

## Download

| Horizon Server version | Download Powercli module |
|------------------------------------------------------------------------------------------------------------------------| --- |
| 8.13/2406 | [horizon4powercli_2406](https://github.com/euc-dev/horizon-powercli/releases/download/2406/horizon4powercli_2406.zip) |

## Supported Powershell versions

1. Windows PowerShell 5.1
2. PowerShell 7.x

## Installation Prerequisites

| OS Type | .Net Version | Powershell Version |
|---|---|---|
| Windows | .NET Framework 4.7.2 or later <br> .NET Core 3.1 | Windows PowerShell 5.1<br>PowerShell 7.x |
| Linux | .NET Core 3.1 | PowerShell 7.x |
| macOS | .NET Core 3.1 | PowerShell 7.x |

## Installation steps

1. Download the horizon powercli zip file.
2. Open PowerShell on your local machine.
3. To view the folder paths to which you can extract the PowerCLI ZIP file, run the command: 

    ```powershell
    $env:PSModulePath
    ```

4. Extract the contents of the PowerCLI ZIP file to one of the listed folders. 

**Important Information:**

Horizon PowerCLI is based on View APIs which are scheduled to be deprecated in future releases. For more information, visit the [Advance Deprecation Announcement for Horizon View API and Replacement with REST API (6000139) KB](https://kb.omnissa.com/s/article/6000139?lang=en_US)
