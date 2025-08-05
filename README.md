# Windows-Sandbox-Tools
Various useful scripts for use within Windows Sandbox

---------

## Using `SandboxStartup.ps1`
The script is written assuming it will be run from _within_ the sandbox, so to automatically run it you'll need to put it into a mapped shared folder.

1. Create some new folder location (not in the sandbox) which you'll map into the sandbox. It doesn't matter what it's called or where it goes, but maybe something like `C:\Users\WhateverUsername\MySharedSandboxFolder`
2. In this repo I have the  [`MyDefaultSandbox.wsb`](Sandbox%20Configurations/MyDefaultSandbox.wsb) configuration file which is already set up to map the folder to the location the script expects. So in there you just need to update the `<HostFolder>` setting to use the path you selected in the previous step. 

    For Example:
    ```
    <HostFolder>C:\Users\WhateverUsername\MySharedSandboxFolder</HostFolder>
    ```
    
3. Update any other options to your liking in the `.wsb` file, such as amount of RAM.
4. Launch Sandbox using the configuration by double clicking `MyDefaultSandbox.wsb`. It will map the folder to the Desktop as a folder called `HostShared`, and run the script automatically. You can also add other scripts and things to the shared folder you may want to run manually.
