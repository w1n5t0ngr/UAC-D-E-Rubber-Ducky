This the official blazing fast UAC-bypassing Rubber Ducky payload generator.

Our Goal.
Our main goal is to silently and FAST download an drop any binary executable to an Windows box,granting it administrate privileges to freely roam the system.

It uses a simple 2 stage process

Stage 1:
Stage one is the script that is triggered when the ducky is connection to any targeted windows machine.
It will execute an powerful one-liner inside the "run" dialog of the system.
The one liner is a simple powershell script, that when executes instantly hides then powershell windows and runs it the background.
The powershell script downloads and execute our stage 2 .vbs payload in the %temp% directory

Stage 2:
Once your .vbs payload is on the system, we proceed to download our main binary payload. The .vbs script exploits a flaw in the windows registry system, this allows us to execute any binary file on the system with admin privilege without prompting the user for access (UAC).

This UAC flaw has been tested working until Windows 10 update 1607 Released LATE 2016.
The lastest update will not cause any issues, as the file will still execute, but it will not execute with admin privileges.
All other Windows systems that have the UAC system is effected by this. 