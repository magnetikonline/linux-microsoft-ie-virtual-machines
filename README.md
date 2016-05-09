# Running IE 7/8/9/10/11/Edge Virtual machines from Microsoft under Linux via VirtualBox
Detailed step-by-step notes for installing the [Microsoft provided Internet Explorer virtual machines](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/) under Linux using VirtualBox.

Has been tested under Ubuntu 14.04LTS (and previously 12.04LTS), with the assumption that VirtualBox is already installed on host.

- [General notes](#general-notes)
- [Available images](#available-images)
	- [IE7 - Vista Enterprise](#ie7---vista-enterprise)
	- [IE8 - XP](#ie8---xp)
	- [IE8 - Windows 7](#ie8---windows-7)
	- [IE9 - Windows 7](#ie9---windows-7)
	- [IE10 - Windows 7](#ie10---windows-7)
	- [IE10 - Windows 8](#ie10---windows-8)
	- [IE11 - Windows 7](#ie11---windows-7)
	- [IE11 - Windows 8.1](#ie11---windows-81)
	- [IE11 - Windows 10](#ie11---windows-10)
	- [MS Edge - Windows 10](#ms-edge---windows-10)
- [Activating images](#activating-images)
- [Rearming images](#rearming-images)
- [Reference](#reference)

## General notes
- Create a new VirtualBox virtual machine, named as desired.
- All images are to be run as **32bit** virtual machines *except* for the following, which are **64 bit**:
	- [IE11 - Windows 10](#ie11---windows-10).
	- [MS Edge - Windows 10](#ms-edge---windows-10).
- Select *Use an existing virtual hard drive file*.
- Pick your downloaded and extracted `*.vmdk` image.
- Apply any image specific system settings as outlined for each IE/OS version combination below.
- You may need to update **VirtualBox Guest Additions** after VM startup to match that of your installed VirtualBox version.
- It's a smart idea to keep a clean copy of each vmdk disk image once the OS usage period ends, to avoid a full image re-download hit.


## Available images

### IE7 - Vista Enterprise
**Note:** Sadly no "IE7 with XP" image has been provided by Microsoft, which *could* have offered a smaller download.

```sh
$ mkdir -p ~/vm/ie7-vista && cd ~/vm/ie7-vista
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie7-vista.txt
$ cat IE7.Vista.For.Linux.VirtualBox.zip.00? >IE7.Vista.For.Linux.VirtualBox.zip
$ unzip IE7.Vista.For.Linux.VirtualBox.zip
$ tar -xf "IE7 - Vista.ova"
$ rm IE7.Vista.For.Linux.VirtualBox.zip* IE7*.ov?
```

- Use the resulting `IE7 - Vista-disk1.vmdk` with VirtualBox.
- Recommended 512MB RAM minimum.
- Image will give a total of 30 days of use, after which you may be able to [rearm the image](#rearming-images).
- **Note:** After creating the VirtualBox machine instance, you *must* go to **Settings - System** and check **Enable I/O APIC** - otherwise the VM most likely won't boot.


### IE8 - XP
```sh
$ mkdir -p ~/vm/ie8-xp && cd ~/vm/ie8-xp
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie8-xp.txt
$ cat IE8.XP.For.Linux.VirtualBox.zip.00? >IE8.XP.For.Linux.VirtualBox.zip
$ unzip IE8.XP.For.Linux.VirtualBox.zip
$ tar -xf "IE8 - WinXP.ova"
$ rm IE8.XP.For.Linux.VirtualBox.zip* IE8*.ov?
```

- Use the resulting `IE8 - WinXP-disk1.vmdk` with VirtualBox.
- Recommended 256MB RAM minimum.
- Image will give a total of 30 days of use, after which you may be able to [rearm the image](#rearming-images).
- **Note:** After creating the VirtualBox machine instance, you *must* go to **Settings - System** and check **Enable I/O APIC** - otherwise the VM most likely won't boot.


### IE8 - Windows 7
```sh
$ mkdir -p ~/vm/ie8-windows7 && cd ~/vm/ie8-windows7
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie8-windows7.txt
$ cat IE8.Win7.For.Windows.VirtualBox.zip.00? >IE8.Win7.For.Linux.VirtualBox.zip
$ unzip IE8.Win7.For.Linux.VirtualBox.zip
$ tar -xf "IE8 - Win7.ova"
$ rm IE8.Win7.For.*.VirtualBox.zip* IE8*.ov?
```

- Use the resulting `IE8 - Win7-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE9 - Windows 7
```sh
$ mkdir -p ~/vm/ie9-windows7 && cd ~/vm/ie9-windows7
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie9-windows7.txt
$ cat IE9.Win7.For.Linux.VirtualBox.zip.00? >IE9.Win7.For.Linux.VirtualBox.zip
$ unzip IE9.Win7.For.Linux.VirtualBox.zip
$ tar -xf "IE9 - Win7.ova"
$ rm IE9.Win7.For.Linux.VirtualBox.zip* IE9*.ov?
```

- Use the resulting `IE9 - Win7-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE10 - Windows 7
```sh
$ mkdir -p ~/vm/ie10-windows7 && cd ~/vm/ie10-windows7
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie10-windows7.txt
$ cat IE10.Win7.For.Linux.VirtualBox.zip.00? >IE10.Win7.For.Linux.VirtualBox.zip
$ unzip IE10.Win7.For.Linux.VirtualBox.zip
$ tar -xf "IE10 - Win7.ova"
$ rm IE10.Win7.For.Linux.VirtualBox.zip* IE10*.ov?
```

- Use the resulting `IE10 - Win7-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE10 - Windows 8
```sh
$ mkdir -p ~/vm/ie10-windows8 && cd ~/vm/ie10-windows8
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie10-windows8.txt
$ cat IE10.Win8.For.Linux.VirtualBox.zip.00? >IE10.Win8.For.Linux.VirtualBox.zip
$ unzip IE10.Win8.For.Linux.VirtualBox.zip
$ tar -xf "IE10 - Win8.ova"
$ rm IE10.Win8.For.Linux.VirtualBox.zip* IE10*.ov?
```

- Use the resulting `IE10 - Win8-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 7
```sh
$ mkdir -p ~/vm/ie11-windows7 && cd ~/vm/ie11-windows7
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows7.txt
$ cat IE11.Win7.For.Linux.VirtualBox.zip.00? >IE11.Win7.For.Linux.VirtualBox.zip
$ unzip IE11.Win7.For.Linux.VirtualBox.zip
$ tar -xf "IE11 - Win7.ova"
$ rm IE11.Win7.For.Linux.VirtualBox.zip* IE11*.ov?
```

- Use the resulting `IE11 - Win7-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 8.1
```sh
$ mkdir -p ~/vm/ie11-windows8.1 && cd ~/vm/ie11-windows8.1
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows8.1.txt
$ cat IE11.Win8.1.For.Linux.VirtualBox.zip.00? >IE11.Win8.1.For.Linux.VirtualBox.zip
$ unzip IE11.Win8.1.For.Linux.VirtualBox.zip
$ tar -xf "IE11 - Win8.1.ova"
$ rm IE11.Win8.1.For.Linux.VirtualBox.zip* IE11*.ov?
```

- Use the resulting `IE11 - Win8.1-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 10
```sh
$ mkdir -p ~/vm/ie11-windows10 && cd ~/vm/ie11-windows10
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows10.txt
$ cat IE11.Win10.For.Linux.VirtualBox.zip.00? >IE11.Win10.For.Linux.VirtualBox.zip
$ unzip IE11.Win10.For.Linux.VirtualBox.zip
$ tar -xf "IE11 - Win10.ova"
$ rm IE11.Win10.For.Linux.VirtualBox.zip* IE11*.ov?
```

- Use the resulting `IE11 - Win10-disk1.vmdk` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).
- **Note:** The Windows 10 base OS is a **64bit** image.
- **Note #2:** The currently available Windows 10/IE11 image has [expired and raised as a bug with Microsoft](https://connect.microsoft.com/IE/feedback/details/1326730/problem-with-windows-10-on-windows-7-virtual-box). As noted, setting your system date **before** April 15th, 2015 will allow this expired image to boot.


### MS Edge - Windows 10
```sh
$ mkdir -p ~/vm/msedge-windows10 && cd ~/vm/msedge-windows10
$ wget -i https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10.txt
$ unzip MSEdge.Win10TH2.VirtualBox.zip
$ tar -xf "IE11 - Win10.ova"
$ rm IE11.Win10.For.Linux.VirtualBox.zip* IE11*.ov?
```

- Use the resulting `MSEdge - Win10TH2-disk1.vmdk` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).
- **Note:** The Windows 10 base OS is a **64bit** image.


## Activating images
For Windows **7, 8, 8.1 and 10** images once connected to the Internet you will need to activate the OS trial to give a full 90 days of use. Enter the following from the Command Prompt running as administrator (Start - Right click Command Prompt - Run as administrator):

```
C:\> slmgr /ato
```

After a short delay you should be presented with a dialog telling you your Windows OS has been successfully activated for a 90 day trial.

## Rearming images
For Windows **XP, Vista and 7** images you *may* be able to extend the initial trial usage period once it has expired via the "rearm" process:

- To rearm a Windows XP image:

	```
	C:\> rundll32.exe syssetup,SetupOobeBnk
	```

- To rearm Windows Vista and 7 images run the following as an administrator:

	```
	C:\> slmgr /rearm
	```

It is not currently possible to rearm the trial period of Windows 8 images.


## Reference
- https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/
- http://modernievirt.blob.core.windows.net/vhd/release_notes_license_terms_1_5_15.pdf
- http://blog.reybango.com/2013/02/04/making-internet-explorer-testing-easier-with-new-ie-vms/
- API endpoint returning latest Microsoft Virtual Machine builds (thanks to [Antón Molleda](https://twitter.com/molant) for the tip):
	- https://developer.microsoft.com/en-us/microsoft-edge/api/tools/vms/
