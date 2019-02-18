# Proxmox_Hassio
Easily install Hassio on Proxmox hyperviser

Download the file vzdump-qemu-HASSIO.2.9.vma.gz and place on your computer somewhere
https://drive.google.com/open?id=1GywVR6ifK3sRgh3sJGV50EGgXAC0uWSr

Download WinSCP		https://winscp.net/download/WinSCP-5.13.7-Setup.exe
open WinSCP and create a new session

File Protocol:			SFTP
Hostname:			proxmox IP Address
Port Number:			22
Username:			root
Password:			<what ever your password is set to>

Once connected, douclick on <var> then click <lib> then click <vz>

If the folder "dump" does not exist click "F7" and enter "dump" and press enter

Then double click on the dump folder to enter it
 
In the left window find the file "vzdump-qemu-HASSIO.2.9.vma.gz" and drag it to the right window
"/var/lib/vz/dump/vzdump-qemu-HASSIO.2.9.vma.gz"

Go into the Proxmox web page, you will see 2 storage devices <local> and <local-lvm> click on <local>

Then in the center column click <Content>
in the right column you should see a <VZDump backup file (1 item)>
click on the file <vzdump-qemu-HASSIO.2.9.vma.gz> and click <Restore>
You will be for a storage location and "VM ID" the VM ID is the computer number starting at 100 

Once Restored right click on the machine and click <Convert to Template>
this will allow you to configure it and clone but not turn it on

Lastley you can clone the machine  XXX(hassio 2.9) and change the 
processors/memory and any other hardware you like
