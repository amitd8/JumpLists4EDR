# JumpLists4EDR
Automate acquisition process of JumpLists Forensic artifact from an endpoint managed by an EDR/XDR **(Tested on Cortex)**.

JumpList is a Windows feature being used by the OS in order to give quick access to recently used files, folders, or tasks relevant to a particular application. These lists appear when you right-click on an application's icon in the taskbar or Start menu.
#### DFIR investigators use this feature as a Forensic artifact that can provide an insight into users actions on the computer
![image](https://github.com/amitd8/JumpLists4EDR/assets/97177937/3894b74f-a828-49fb-bc9a-925bf387bf69)



The script leverages the abilities of [JLECMD.exe](https://github.com/EricZimmerman/JLECmd), by deploying it in order to perform a quickscan, than deletes the EXE from disk.

#### Output Data will be saved as a CSV located in the root of the OS (Usually C:\), CSV later can be loaded in TimelimeExplorer for further analysis
## Installation (for Cortex XDR)
###### Running the script not as unprivileged user or inputing a user that isn't available on the endpoint will result in Error

The script must be uploaded directly on the Cortex XDR console in Response / Action Center / Scripts Library:
1. Click on the **New Script** button and upload the script.
2. **Script Name** could be any name or description.
3. **Supported OS** must be Windows.
5. **Timeout** could be configured to any value you want but starting with 600 seconds is more than enough.
6. **Input** must be set to **Run by entry point** with **main** as an entry point. user is a string.
7. **Output Type** must be **Auto Detect**

