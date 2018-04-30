# A Framework of Scripts and tools to automate Live Incident Response


Key features include:

- Acquisistion of Physical memory (via dumpit.exe) capturing kernel and user space
- Runs a series of live tools (mostly WinSysinternal and System32 tools) enumerating a system and collecting all pertinent information such as: networking information, important system events - such as new user added, networking information, File MAC times, startup programs, scheduled tasks and much more
- Option to check tool integrity (via fciv.exe)
- Option to check C:\Windows\System32 Dll integrity (due to Windows known DLL feature it is almost impossible to run any program on Windows without using DLL's from C:\Windows\System32 so it is a very good idea to check DLL's to avoid inadvertantly loading a compromised DLL



Useage:

Simply plugin the USB Drive and run the .bat script runme_as_admin_x64.bat ad administrator and it will launch a cmd window which will guide you through the process

If you wish to add your own tools or change existing tools you will need to run generate_hashes.bat (in tools folder) to generate new hashes.

****it is improtant the sytem32 folder on USB matches the one on the system you are investigating, copy one form a trusted system with matching OS version, run generate_hashes.bat (tools folder) to generate a new XML file containing the new hash values

