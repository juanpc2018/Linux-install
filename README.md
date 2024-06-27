## Linux-install

for Beginners.</br>

Windows is Internal but Linux can be Internal or External "Portable" </br>
there are Pros and Cons. 

1st you need to know the basic differences,</br>
then you can understand the Pros and Cons</br>
then you can [find](https://distrowatch.com/) your favorite Linux.</br>

If installing Linux on a Internal SSD/M.2 drive: </br>
#1. requires to set BIOS/UEFI to allow AHCI in laptops with Optane,</br>
or wont detect or boot the SSD/M.2.</br>
usually [Control+S] in Main BIOS/Menu or similar to make visible the menu. </br>
#2. Disable [Secure Boot](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-secure-boot) </br>
Secure Boot Active/Enabled, Only allows to Boot internally from the OEM OS pre-installed at factory. </br>

Linux can also be installed "Portable" on a External SSD/M.2 </br>
IF using a USB pen drive as main, Linux will be very slow, flash memory is Not recommended. </br>
IF using a USB SSD/M.2 drive, will run max at 500MB/s in USB3.0 "fast enough" </br>
IF using a USB HDD 2.5" drive, will run slower 160MB/s on USB3.0 "Not fast" </br>
IF using a Thunderbolt3 case drive with SSD/M.2, will run faster than USB3.0 </br>
IF using a Thunderbolt2 SSD/M.2 will run slower If using a TB3 to TB2 adapter. </br>
USB4.0 with Thunderbolt3 is Optional, Not all machines with USB4 have it. </br>

When formatting SSD/M.2 the 1st time "Clean Install" </br>
Linux allows to format the drive with different File Systems. </br>
does Not have a fixed FileSystem like other OS. </br>
Windows has NTFS since 7, ReFS for Servers. </br>
OSX since 10.6 SnowLeopard has HFS+ </br>
OSX since 10.13 HighSierra has APFS </br>

Linux has Ext4, the most common FileSystem, </br>
but Newer Ext4 since Linux >16 is Not backward compatible with older Ext4 v1.0 </br>
its should have been called Ext5 in my opinion. </br>

New Ext4 makes weird sounds when formatting a Large HDD 18TB, because the strict Journaling. </br>
Jurnaling means that the drive stores the changes about to be made by the OS, like a Log </br>
if there is a problem like a power failure, FileSystem can see and auto-correct the errors </br>
without Journaling, errors need to be corrected manually or hdd wont write as a protection measure. </br>
different FS have different methods how to implement Journaling. </br>
some very strict at time of format, others as drive gets filled. </br>

Btrfs has interesting features, ZFS... </br>
XFS is the FileSystem i prefer, at least for large HDDs. </br>

There is software that allows to Read/Write Ext4 old & New Ext4 in Windows </br>
Ext2Fsd 0.69 works in Windows7/8/10 R/W Old Ext4 v1.0 </br>
Ext2Fsd 0.71 is a fork, New Ext4 but a work in progress. Read Only, Write with Caution. </br>

Linux allows to Read & Write many file systems: </br>
Ext4, NTFS, ExFAT, FAT32, Btrfs, XFS, ZFS, HFS+, APFS with optional Paragon drivers, etc... </br>
if want to Read/Write in 1 Machine all FileSystems = Not recommended. </br>
for 100% compatibility is better to have multiple machines connected by Ethernet 1Gbe or faster. </br>
10G SFP+ fiber optic goes at 1200MB/s direct, or 500MB/s using a Router with a slow dual core 600MHz cpu. </br>

Each OS has a different methods to see the other machines with Samba SMB v1 v2 v3 </br>
Windows needs to manually activate Samba in Powershell, </br>
SMB drives cannot be seen with Windows Network File Manager, like Normal Windows Network. </br>
needs to access manually typing the IP addres on Run Command: ./192.168.1.1 </br>

------------------

There are many different Linux versions: </br>
Debian type "DEB" </br>
RedHat Type "RPM" </br>
Arch type </br>
BSD type. </br>

RPM is usually for servers, corporations using POWER9 CPUs. </br>
Debian is the most common Linux type. </br>
BSD, and Arch. </br>
BSD forked in different OS, for Sony PlayStation4, Mac OSX, etc... </br>

software written for RPM can be converted to DEB with Alien app. </br>
Distros like [T2 SDE](https://t2sde.org/download/) are available for many different CPU architectures. </br>
x86_64, Motorola 68K, MIPS, Arm aarch64, etc... </br>
There are Distros that only support 1 type of CPU, like [Asahi Linux](https://asahilinux.org/about/) for M1 M2 CPUs.

in Debian there are many branches, most are for x86_64 CPUs Intel or AMD. </br>
custom designed with pre-installed software for different type of users: </br>
Office, Video editing, Sound DAW, Gaming or Clean Type, No pre-installed software. </br>
Barebone DIY. </br>

the most popular Debian Distro is Ubuntu. </br>
but there is also other branches: Kubuntu, Xubuntu, Lubuntu, Wubuntu, etc... </br>
The main difference is the "Desktop Environment" </br>
Linux allows to have different flavours of Desktop. </br>
 
KDE is the most popular Desktop, Gnome, Cinnamon "a fork of Gnome", MATE, Xfce, etc... </br>
different Distros come with different Desktops pre-installed. </br>
Linux allows to instal other if desired, for example: </br>
[MaXX](https://docs.maxxinteractive.com/) based on the sgi [IRIX](https://en.wikipedia.org/wiki/IRIX) OS, but requires NVIDIA GPU. </br>

there are other differences, like the size of the Virtual memory, SWAP file, etc... </br>
but that can be changed by the user. </br>

is Not only a superficial change, is also functional </br>
for example:  </br>
Ubuntu GNOME Desktop has Nautilus File Browser/Manager. </br>
Kubuntu KDE Plasma Desktop has Dolphin File Manager. </br>
both "do the same" but work a bit different. </br>
in Nautilus when typing a letter: automatically search & filter results. </br>
in Dolphin when typing a letter: jumps to 1st folder or file with that letter. </br>
there are many others, like Neon Desktop, etc... </br>

### The basic method to install Linux: </br>
#1. download any .iso example: [.torrent](https://kubuntu.org/alternative-downloads/) the fastest method. </br>
#2. download an .iso burner to USB pen drive </br>
like BalenaEtcher, Rufus, and many others. </br>
#3. burn the .iso to USB pen drive usually 8GB or more. </br>
#4. ReBoot machine. </br>
#5. Press F11 / F12 or similar "depends on the machine BIOS brand", </br>
to activate the: Boot menu. </br>
#6. select the USB pen drive. </br>
#7. Boot from the USB pen drive.  </br>

there are more steps but those depend on your install method: </br>
Internal or External. </br>

Not all Linux work in all machines </br>
depends on the Kernel version, </br>
Kernel 6.0 or more has modern hardware support, and some old HW support was deleted. </br>

### other install methods: </br>
people that want to install / test different .isos </br>
instead of burning each individually to many slow Pen Drives </br>
use a software called Ventoy, that allows to Boot from a large HDD </br>
and have multiple .isos Unburned, and select a menu what .iso to Boot. </br>
much better option if want to try different Distros. </br>

### Installing Internal 2 ways: </br>

A) Creating a Partition on the same Windows install "Not Recommended" Advanced user only. </br>
B) installing to another SSD / M.2 drive </br>
some machines allow to install 2x SSD/M.2 internally, </br>
some machines only have 1 slot and require to manually uninstall the old SSD/M.2. </br>

machines with only 1 internal SSD/M.2 is better to install Linux to External drive. </br>
unless you want the extra speed 500MB/s USB3 vs. 1600MB/s 2500MB/s 5000MB/s of PCIe v2 v3 v4 v5 </br>
and does Not have Thunderbolt3 port. </br>

iFix it has many tutorials how to unscrew many machines, </br>
if want to open and install a New SSD/M.2 drive. </br>

### Installing External:

USB3 cases from Orinco are very nice, have RTL9210 controller </br>
BUT... M.2 NVMe drives used external require a High [Efficiency (MB/s per Watt)](https://www.tomshardware.com/reviews/pny-xlr8-cs3140-ssd-review/2) </br>
400MB/s Watt minimum, 300MB/s will overheat and get partially damaged when moving large files >100GB. </br>
Orinco cases have a Heatsink but some M.2 drives are 1 or 2mm bigger on the sides, </br>
needs to open 1 leg of the heatsink wider with pliers, before installing the M.2 </br>

----------------------

Software i recommend installing: </br>
$ snap install cpufetch </br>
$ apt install cpupower-gui </br>
$ apt install cpu-x </br>
Synaptic package manager </br>
Spectacle screen capture or Shutter </br>
$ apt install neofetch </br> 
Kpatience "solitaire" </br>
Warpinator "Wi-Fi file transfer between Android, Linux, and Windows" requires Router with open ports. </br>
BlockOut II "3D Tetris" </br>
OBS Studio "video screen capture record & streaming" </br>
Okular "pdf viewer" </br>
GIMP "Photoshop alternative" </br>
InkSkape "Vector alternative to CorelDraw, Adobe ilustrator" </br>
Krita "GIMP alternative"  </br>
[OpenOffice](https://www.openoffice.org/download/index.html) or LibreOffice </br>
SuperTux "SuperMario 2D scroller type" </br>
Extreme Tux Racer "3D OpenGL Winter Games" works with intel iGPUs </br>
Timidity "MIDI Player" </br>

#### Optional: </br>
Signal Desktop </br>
Skype </br>
ALSA Focursire Control Panel </br>

#### Browsers: </br>
Yandex </br>
Firefox </br>
LibreWolf </br>
ArticFox </br>
Opera </br>
Vivaldi </br>
Chromium </br>
Brave </br>
Thorium </br>
MeetSideKick </br>
Tor </br>
etc... </br>
