# PowerShell

![Powershell logo](PowerShell_5.0_icon.png)

## Essential Commands and Aliases
|Task|Cmdlet|Common Aliases|
|---|---|---|
|Get help|`Get-Help <Command-Name>`|`man`|
|List commands|`Get-Command`| |
|Get current location|`Get-Location`|`pwd`|
|Change location|`Set-Location <Path>`|`cd`|
|List directory contents|`Get-ChildItem`|`ls`, `dir`, `gci`|
|Get file content|Get-Content <File-Path>|`gc`, `cat`|
|Copy items |`Copy-Item <Source> <Destination>` |`cp`, `cpi` |
|Move items |`Move-Item <Source> <Destination>`|`mv`, `mi` |
|Remove items |`Remove-Item <Name>` |`rm` |
|Create new item |`New-Item <Name>` |`mkdir`, `touch` |
|Manage processes |`Get-Process`, `Stop-Process` ||
|Manage services |`Get-Service`, `Start-Service` ||
# About PowerShell

[__PowerShell__](https://docs.microsoft.com/en-us/powershell/ ) is a powerful command-line shell and scripting language developed by Microsoft. It is designed to help users automate tasks, manage systems, and perform administrative tasks efficiently. Built on the [.NET framework](https://learn.microsoft.com/en-us/dotnet/framework/get-started/overview ), __PowerShell__ is both a ***command-line tool*** and ***a scripting environment***, making it a versatile tool for programmers and system administrators.

> "PowerShell is great because we had a series of rockstar engineers add their awesomeness to the project."
>  
> Source: from the [interview](https://evrone.com/blog/jeffrey-snover-interview) with Jeffrey Snover, PowerShell Inventor

## Why Learn PowerShell?
PowerShell is an essential tool for:
1. Automating repetitive tasks.
2. Managing and configuring systems.
3. Working with files, processes, and services.
4. Interacting with APIs and web services.
5. Writing scripts to solve complex problems.

## PowerShell Features and Terms
* __Cmdlets__: Lightweight commands that perform specific functions.
* __Scripting__: Write and execute scripts, series of commands, to automate tasks.
* __Pipeline__: Chain commands together to pass data between them using |.
* __Remote Management__: Execute commands on remote systems.
* __Modules__: Extend functionality with additional cmdlets and scripts.
* __Extensibility__: Create custom functions, modules, and scripts.
* __Cross-Platform__: PowerShell Core runs on Windows, macOS, and Linux.

## PowerShell History

### PowerShell Version Comparison

|Version|Release Year|Key Features|   
|---|---|---|                      
|1.0|2006|Initial release Windows XP SP2 and Windows Server 2003|
|2.0|2009|Introduced remote management and modules|
|5.1|2016|Last Windows-only version|               
|6.0|2018|Known as PowerShell Core 6.0. First cross-platform version|
|7.0|2020|Unified Windows PowerShell and PowerShell Core, offering a modern, cross-platform experience|

### Version Summary
* __Windows PowerShell__: Versions 1.0 to 5.1 (Windows-only).
* __PowerShell Core__: Versions 6.0 and above (cross-platform).


# PowerShell for Beginners

### Basic Commands to Get Started

* `Get-Command`: Lists all available commands.
* `Get-Help`: Provides help information for commands.
* `Get-Process`: Displays all running processes.
* `Stop-Process`: Stops a specific process.
* `Set-Location`: Changes the current directory (like cd in Command Prompt).
* `New-Item`: Creates a new file or directory.

### Example Script

Here’s a simple script to list all files in a directory and display their sizes:
```
# Get all files in the current directory
$files = Get-ChildItem
    
# Display file names and sizes
foreach ($file in $files) {
Write-Output "$($file.Name) - $($file.Length) bytes"
}
```
### Editors for PowerShell Scripting

When writing and debugging PowerShell scripts, using a dedicated editor can greatly enhance your productivity. Here are two popular options:

### Windows PowerShell Integrated Scripting Environment (ISE)

* __What it is__: A built-in editor for Windows PowerShell (versions 1.0 to 5.1).
* __Features__:
    * Syntax highlighting.
    * Debugging tools (breakpoints, step-through execution).
    * Integrated console for testing scripts.
    * Multi-tab interface for working with multiple scripts.
* __Best for__: Beginners and users working on older versions of PowerShell.

![ISE image](ISE_panes.png)

### Visual Studio Code (VS Code)

* __What it is__: A free, open-source, cross-platform code editor by Microsoft.
* __Features__:
    * Syntax highlighting and IntelliSense for PowerShell.
    * Integrated terminal for running scripts.
    * Extensions for additional functionality (e.g., PowerShell extension).
    * Support for Git and other version control systems.
    * Cross-platform (Windows, macOS, Linux).
* __Best for__: Modern PowerShell development, especially with PowerShell 7 and cross-platform scripting.

![vscode image](vs_code.png)
