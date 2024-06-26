## Linux-install

for Begginers.

Windows is Internal.
but Linux can be Interal or External "Portable"
there are Pros and Cons.

IF installing on a internal SSD/M.2 drive
#1. requires to set BIOS/UEFI to allow AHCI in laptops with Optane,
or wont detect the SSD/M.2.

Linux can also be installed "Portable" on a External SSD/M.2
IF using a USB pen drive as main, Linux will be very slow, flash memory is Not recommended.
IF using a USB SSD/M.2 drive, will run max at 500MB/s in USB3.0 "fast enough"
IF using a USB HDD 2.5" drive, will run slower 160MB/s on USB3.0 "Not fast"
IF using a Thunderbolt3 case drive, will run faster than USB3.0
IF using a Thunderbolt2 will run slower.
USB4.0 Thunderbolt3 is Optional, Not default.

when formatting SSD/M.2 the 1st time "Clean Install"
Linux allows to formatt the drive in different File Systems.
does Not have a fixed FileSystem like other OS.

Ext4 is the most common FS, but Newer Ext4 since Linux >16 is Not backward compatible with older Ext4 v1.0
New Ext4 has weird sounds when formatting a Large HDD 18TB, because the strict preempt Journaling.
Btrfs has interesting features.
XFS is the FS i prefer, at least for large HDD.

there is software that allows to Read/Write Ext4 old & New "64-Bit magic numbers",
Ext2Fsd 0.69 works in Windows to R/W Old Ext4 v1.0
Ext2Fsd 0.71 is a fork, and a work in progress. Read Only, Write with caution.

if you want to Read in 1 Machine all FileSystems = Not recommended,
for 100% compatibility is better to have multiple machines connected by Ethernet 1Gbe or faster.
10G SFP+ fiber optic goes at 1200MB/s direct, or 500MB/s using a Router with a dual core 600MHz cpu.

Each OS has a different methods to see the other machines with Samba SMB v1 v2 v3
Windows needs to manually activate Samba in Powershell,
and drives cannot be seen with Windows Network File Manager,
needs to access manually tiping the IP addres on Commnad ./192.168.1.1
"its Hidden, Not easy access"

There are many different Linux versions:
Debian type "DEB", RedHat Type "RPM", Arch type, BSD type.

RPM is usually for servers, corporations using POWER9 CPUs.
Debian is the most common Linux type.
BSD, and Arch.

software written for RPM can be converted to DEB with Alien app.

in Debian World, there is also many branches,
custom designed with pre-installed software for different type of users.
Office, Video editing, Sound DAW or Clean Type, with No pre-installed software.
Barebone.

the most popular Debian Type Distro is Ubuntu.
but there is also other branches: Kubuntu, Xubuntu, Lubuntu, etc...
the main difference is the "Desktop Environment"
Linux allows to have different flavours of Desktop,
 
KDE is the most popular Desktop, Gnome, Cinnamon "a fork of Gnome", MATE, Xfce, etc...
different Distros come with different Desktop environments pre-installed.
Linux allows to instal other if desired, like for example:


but there are other differences with Virtual memory management.

