

******* Files: *******
amagent-latest.x86_64.rpm - Automox installer for Linux
-Guest script configuration name = "vRO - Lnx - Automox agent install from vRO Server"

AutomoxInstaller.msi - Automox installer for Windows
-Guest script configuration name = "vRO - Win - Automox agent install from vRO Server"

platform-2.dms - Cyberreason installer for Tenet Linux
-Guest script configuration name = "Tenet - Lnx - Cybereason agent install from vRO server"

puppet_6.19.1_install_packages.tar.gz - Puppet 6.19.1 installers for RHEL6, RHEL7 and RHEL8
-Guest script configuration name = "vRO - Lnx - Puppet 6.19.1 agent install from vRO server"

puppet_install_packages.tar.gz - Puppet 6.10 installers for RHEL6, RHEL7 and RHEL8
-Guest script configuration name = "vRO - Lnx - Puppet agent install from vRO server"

puppet-agent-6.10.0-x64.msi - Puppet 6.10 installer for Windows
-Guest script configuration name = "vRO - Win - Puppet agent install from vRO server"

puppet-agent-6.19.1-x64.msi - Puppet 6.19.1 installer for Windows
-Guest script configuration name = "vRO - Win - Puppet 6.19.1 agent install from vRO server"


******* How to import files as Resource Elements: *******
Use WinSCP (https://winscp.net/) and connect to the vRO Server
Upload file to:
--vRO 7.4 = /var/run/vco/
--vRO 8+  = /data/vco/var/run/vco/
Run workflow "Create Resource file from vRO server file"
--vRoFilePath - replace <FILE> with the filename of the file you uploaded
--mimeType - select x-sh for .sh files, select octet-stream for all other files
--Delete vRO server file after resource file is created? - select Yes
Click Submit


******* How to update Guest script configuration *******
Run workflow "Edit script configuration"
--select the Guest script configuration name
--click Next
--click Next
--click the "File to copy" field 
--Filter and double click the Resource Element file name
--Click Submit


