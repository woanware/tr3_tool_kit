TR3Secure Volatile Data Collection Kit

***** note ******
the executables' names in the tools folder has to match the names of the executables listed below. If they don't match then the script won't work properly
***** note ******

Dependencies

Script Operating Related
	mkdir.exe:           Included in UnxUtils package and located at http://unxutils.sourceforge.net/
	robocopy.exe:        Included in the Windows 2003 resource tool kit and located at http://www.microsoft.com/download/en/details.aspx?id=17657
	whoami: 			 Included in Windows OS on Windows 7
	at.exe               Included in Windows OS on Windows 7
	schtasks.exe         Included in Windows OS on Windows 7
	driverquery.exe      Included in Windows OS on Windows 7
	xcopy.exe            Included in Windows OS on Windows 7
	
Offline Data
	rawcopy.exe 			https://github.com/jschicht/RawCopy (ensure you have both RawCopy64.exe and RawCopy.exe)
	ExtractUsnJrnl			https://github.com/jschicht/ExtractUsnJrnl (ensure you have both ExtractUsnJrnl64.exe and ExtractUsnJrnl.exe)
	
Forensic Imaging Memory Related
	winpmem acquisition tool  Located at http://code.google.com/p/volatility/downloads/list **rename binary to winpmem.exe ***
	
Networking Information Related
	arp.exe:             Located in Windows\System32 folder
	ipconfig.exe:        Located in Windows\System32 folder
	nbtstat.exe:         Located in Windows\System32 folder
	net.exe:             Located in Windows\System32 folder
	netstat.exe:         Located in Windows\System32 folder
	pslist.exe:          Included in Sysinternals PSTools and located at http://technet.microsoft.com/en-us/sysinternals/bb896649.aspx
	
Process Information Related
	CProcess.exe :       Located at http://www.nirsoft.net/utils/cprocess.html
	handle.exe:          Located at http://technet.microsoft.com/en-us/sysinternals/bb896655
	listdlls.exe:        Located at http://technet.microsoft.com/en-us/sysinternals/bb896656
	openports.exe:       Located at http://majorgeeks.com/OpenPorts_d3950.html
	pslist.exe:          Included in Sysinternals PSTools and located at http://technet.microsoft.com/en-us/sysinternals/bb896649.aspx
	tasklist.exe:        Located in Windows\System32 folder
	tcpvcon.exe:         Located at http://technet.microsoft.com/en-us/sysinternals/bb897437
	
Logged On User Information
	psloggedon.exe:      Included in Sysinternals PSTools and located at http://technet.microsoft.com/en-us/sysinternals/bb896649.aspx
	net.exe:             Located in Windows\System32 folder
	logonsessions.exe:   Located at http://technet.microsoft.com/en-us/sysinternals/bb896769

Opened Files Information
	openedfilesview.exe: Located at http://www.nirsoft.net/utils/opened_files_view.html
	psfile.exe:          Included in Sysinternals PSTools and located at http://technet.microsoft.com/en-us/sysinternals/bb896649.aspx

Misc Information
	pclip.exe:           Included in UnxUtils package and located at http://unxutils.sourceforge.net/

System Information
	ver.exe:             Included in Windows OS
	uptime.exe:          Located at http://support.microsoft.com/kb/232243
	ipconfig.exe:        Located in Windows\System32 folder
	urlprotocolview.exe: Located at http://www.nirsoft.net/utils/url_protocol_view.html
	promiscdetect.exe:   Located at http://ntsecurity.nu/toolbox/promiscdetect/
	
Non-Volatile System Information
	autorunsc.exe:       Located at http://technet.microsoft.com/en-us/sysinternals/bb963902
	gplist.exe:          Located at http://ntsecurity.nu/toolbox/gplist/
	gpresult.exe:        Included in Windows OS
	dd.exe		     Included in UnxUtils package and located at http://unxutils.sourceforge.net/
	mmls.exe (also copy zlib1.dll and libewf.dll along with mmls.exe into the tools folder) Located at http://www.sleuthkit.org/sleuthkit/download.php

Admin Error Check
	whoami: Included in Windows OS on Windows 7
	
Batch Script Configuration

1. Nothing needs to be done for the programs located in the system32 folder. The batch script uses the executables on the target system.
2. The remaining programs need to be placed into a sub-folder named tools
3. Customize the antivirus log collection for your environment. For demo purposes the script collects McAfee logs and quarantine folder
3. Change the file extension on the batch script from txt to bat

Executing the Batch Script
1. Open a command prompt with admin rights
2. Change directories to where the scripts are located
3. Execute one of the commands below:

tr3-collect.bat [case number] [drive letter for storing collected data] [menu selection #]

or

tr3-collect-user.bat [path to store collected data] [user profile name]