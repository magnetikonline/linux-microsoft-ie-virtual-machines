# Running IE 7/8/9/10/11/Edge Virtual machines from Microsoft under Linux via VirtualBox
Detailed step-by-step notes for installing the [Microsoft provided Internet Explorer virtual machines](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/) under Linux using VirtualBox.

Has been tested under Ubuntu 16.04LTS (previously 14.04LTS) with [VirtualBox](https://www.virtualbox.org) version 5.1.

- [General notes](#general-notes)
- [Available images](#available-images)
	- [IE6 - Windows XP](#ie6---windows-xp)
	- [IE7 - Vista Enterprise](#ie7---vista-enterprise)
	- [IE8 - Windows XP](#ie8---windows-xp)
	- [IE8 - Windows 7](#ie8---windows-7)
	- [IE9 - Windows 7](#ie9---windows-7)
	- [IE10 - Windows 7](#ie10---windows-7)
	- [IE10 - Windows 8](#ie10---windows-8)
	- [IE11 - Windows 7](#ie11---windows-7)
	- [IE11 - Windows 8.1](#ie11---windows-81)
	- [IE11 - Windows 10](#ie11---windows-10)
	- [MS Edge - Windows 10 Stable (13.10586)](#ms-edge---windows-10-stable-1310586)
	- [MS Edge - Windows 10 Preview (14.14342)](#ms-edge---windows-10-preview-1414342)
	- [MS Edge - Windows 10 Stable (14.14393)](#ms-edge---windows-10-stable-1414393)
	- [MS Edge - Windows 10 Preview (15.14959)](#ms-edge---windows-10-preview-1514959)
	- [MS Edge - Windows 10 Preview (15.15014)](#ms-edge---windows-10-preview-1515014)
	- [MS Edge - Windows 10 Preview (15.15063)](#ms-edge---windows-10-preview-1515063)
	- [MS Edge - Windows 10 Stable (16.16299)](#ms-edge---windows-10-stable-1616299)
- [Activating images](#activating-images)
- [Rearming images](#rearming-images)
- [Reference](#reference)

## General notes
- Download, re-construct and decompress archive image as per each images instructions below.
- From VirtualBox goto `File` -> `Import Appliance...`
- Select the decompressed Open Virtualization Format `ovf` file.
- Review virtual machine name and settings (adjusting to suit if required), then click `Import`.
- Before starting the image, create a snapshot of the current machine state - this will allow you to quickly roll back to a fresh virtual machine once the usage period of the OS expires.
- All images are **32bit** virtual machines *except* for the following, which are **64 bit**:
	- [IE7 - Vista Enterprise](#ie7---vista-enterprise)
	- [IE11 - Windows 10](#ie11---windows-10)
	- [MS Edge - Windows 10 Stable (13.10586)](#ms-edge---windows-10-stable-1310586)
	- [MS Edge - Windows 10 Preview (14.14342)](#ms-edge---windows-10-preview-1414342)
	- [MS Edge - Windows 10 Stable (14.14393)](#ms-edge---windows-10-stable-1414393)
	- [MS Edge - Windows 10 Preview (15.14959)](#ms-edge---windows-10-preview-1514959)
	- [MS Edge - Windows 10 Preview (15.15014)](#ms-edge---windows-10-preview-1515014)
- You may need to update the images installed **VirtualBox Guest Additions** after VM startup to match that of your VirtualBox version.
- It's a smart idea to keep a clean copy of each `ovf` disk image once the OS usage period ends, to avoid a full image re-download hit.


## Available images

### IE6 - Windows XP
```sh
$ mkdir -p ~/vm/ie6-windowsxp && cd ~/vm/ie6-windowsxp
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie6-windowsxp.txt
$ cat IE6.XP.For.Linux.VirtualBox.zip.00? >IE6.XP.For.Linux.VirtualBox.zip
$ rm ie6-windowsxp.txt IE6.XP.For.Linux.VirtualBox.zip.00?
$ unzip IE6.XP.For.Linux.VirtualBox.zip
$ rm IE6.XP.For.Linux.VirtualBox.zip
```

- Use the resulting `IE6 - WinXP.ova` with VirtualBox.
- Recommended 256MB RAM minimum.
- Image will give a total of 30 days of use, after which you may be able to [rearm the image](#rearming-images).


### IE7 - Vista Enterprise
**Note:** Sadly no "IE7 with XP" image has been provided by Microsoft, which *could* have offered a smaller download.

```sh
$ mkdir -p ~/vm/ie7-vista && cd ~/vm/ie7-vista
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie7-vista.txt
$ cat IE7.Vista.For.Linux.VirtualBox.zip.00? >IE7.Vista.For.Linux.VirtualBox.zip
$ rm ie7-vista.txt IE7.Vista.For.Linux.VirtualBox.zip.00?
$ unzip IE7.Vista.For.Linux.VirtualBox.zip
$ rm IE7.Vista.For.Linux.VirtualBox.zip
```

- Use the resulting `IE7 - Vista.ova` with VirtualBox.
- Recommended 512MB RAM minimum.
- Image will give a total of 30 days of use, after which you may be able to [rearm the image](#rearming-images).


### IE8 - Windows XP
```sh
$ mkdir -p ~/vm/ie8-windowsxp && cd ~/vm/ie8-windowsxp
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie8-windowsxp.txt
$ cat IE8.XP.For.Linux.VirtualBox.zip.00? >IE8.XP.For.Linux.VirtualBox.zip
$ rm ie8-windowsxp.txt IE8.XP.For.Linux.VirtualBox.zip.00?
$ unzip IE8.XP.For.Linux.VirtualBox.zip
$ rm IE8.XP.For.Linux.VirtualBox.zip
```

- Use the resulting `IE8 - WinXP.ova` with VirtualBox.
- Recommended 256MB RAM minimum.
- Image will give a total of 30 days of use, after which you may be able to [rearm the image](#rearming-images).


### IE8 - Windows 7
```sh
$ mkdir -p ~/vm/ie8-windows7 && cd ~/vm/ie8-windows7
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie8-windows7.txt
$ cat IE8.Win7.For.Windows.VirtualBox.zip.00? >IE8.Win7.For.Linux.VirtualBox.zip
$ rm ie8-windows7.txt IE8.Win7.For.Windows.VirtualBox.zip.00?
$ unzip IE8.Win7.For.Linux.VirtualBox.zip
$ rm IE8.Win7.For.Linux.VirtualBox.zip
```

- Use the resulting `IE8 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE9 - Windows 7
```sh
$ mkdir -p ~/vm/ie9-windows7 && cd ~/vm/ie9-windows7
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie9-windows7.txt
$ cat IE9.Win7.For.Linux.VirtualBox.zip.00? >IE9.Win7.For.Linux.VirtualBox.zip
$ rm ie9-windows7.txt IE9.Win7.For.Linux.VirtualBox.zip.00?
$ unzip IE9.Win7.For.Linux.VirtualBox.zip
$ rm IE9.Win7.For.Linux.VirtualBox.zip
```

- Use the resulting `IE9 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE10 - Windows 7
```sh
$ mkdir -p ~/vm/ie10-windows7 && cd ~/vm/ie10-windows7
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie10-windows7.txt
$ cat IE10.Win7.For.Linux.VirtualBox.zip.00? >IE10.Win7.For.Linux.VirtualBox.zip
$ rm ie10-windows7.txt IE10.Win7.For.Linux.VirtualBox.zip.00?
$ unzip IE10.Win7.For.Linux.VirtualBox.zip
$ rm IE10.Win7.For.Linux.VirtualBox.zip
```

- Use the resulting `IE10 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE10 - Windows 8
```sh
$ mkdir -p ~/vm/ie10-windows8 && cd ~/vm/ie10-windows8
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie10-windows8.txt
$ cat IE10.Win8.For.Linux.VirtualBox.zip.00? >IE10.Win8.For.Linux.VirtualBox.zip
$ rm ie10-windows8.txt IE10.Win8.For.Linux.VirtualBox.zip.00?
$ unzip IE10.Win8.For.Linux.VirtualBox.zip
$ rm IE10.Win8.For.Linux.VirtualBox.zip
```

- Use the resulting `IE10 - Win8.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 7
```sh
$ mkdir -p ~/vm/ie11-windows7 && cd ~/vm/ie11-windows7
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows7.txt
$ cat IE11.Win7.For.Linux.VirtualBox.zip.00? >IE11.Win7.For.Linux.VirtualBox.zip
$ rm ie11-windows7.txt IE11.Win7.For.Linux.VirtualBox.zip.00?
$ unzip IE11.Win7.For.Linux.VirtualBox.zip
$ rm IE11.Win7.For.Linux.VirtualBox.zip
```

- Use the resulting `IE11 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 8.1
```sh
$ mkdir -p ~/vm/ie11-windows8.1 && cd ~/vm/ie11-windows8.1
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows8.1.txt
$ cat IE11.Win8.1.For.Linux.VirtualBox.zip.00? >IE11.Win8.1.For.Linux.VirtualBox.zip
$ rm ie11-windows8.1.txt IE11.Win8.1.For.Linux.VirtualBox.zip.00?
$ unzip IE11.Win8.1.For.Linux.VirtualBox.zip
$ rm IE11.Win8.1.For.Linux.VirtualBox.zip
```

- Use the resulting `IE11 - Win8.1.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 10
**Important:** This [image has expired](https://connect.microsoft.com/IE/feedback/details/1326730/problem-with-windows-10-on-windows-7-virtual-box) and raised as a bug with Microsoft. As noted (and have personally confirmed), setting your host system clock anytime **before** `April 15th, 2015` will allow the image to boot. Unfortunately you will need to do this _each and every_ image bootup.

```sh
$ mkdir -p ~/vm/ie11-windows10 && cd ~/vm/ie11-windows10
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/ie11-windows10.txt
$ cat IE11.Win10.For.Linux.VirtualBox.zip.00? >IE11.Win10.For.Linux.VirtualBox.zip
$ rm ie11-windows10.txt IE11.Win10.For.Linux.VirtualBox.zip.00?
$ unzip IE11.Win10.For.Linux.VirtualBox.zip
$ rm IE11.Win10.For.Linux.VirtualBox.zip
```

- Use the resulting `IE11 - Win10.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Stable (13.10586)
```sh
$ mkdir -p ~/vm/msedge-windows10-13.10586 && cd ~/vm/msedge-windows10-13.10586
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-13.10586.txt
$ unzip MSEdge.Win10TH2.VirtualBox.zip
$ rm msedge-windows10-13.10586.txt MSEdge.Win10TH2.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10TH2.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (14.14342)
```sh
$ mkdir -p ~/vm/msedge-windows10-14.14342 && cd ~/vm/msedge-windows10-14.14342
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-14.14342.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-14.14342.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_14342.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Stable (14.14393)
```sh
$ mkdir -p ~/vm/msedge-windows10-14.14393 && cd ~/vm/msedge-windows10-14.14393
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-14.14393.txt
$ unzip MSEdge.Win10_RS1.VirtualBox.zip
$ rm msedge-windows10-14.14393.txt MSEdge.Win10_RS1.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.14959)
```sh
$ mkdir -p ~/vm/msedge-windows10-15.14959 && cd ~/vm/msedge-windows10-15.14959
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-15.14959.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-15.14959.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.15014)
```sh
$ mkdir -p ~/vm/msedge-windows10-15.15014 && cd ~/vm/msedge-windows10-15.15014
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-15.15014.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-15.15014.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.15063)
```sh
$ mkdir -p ~/vm/msedge-windows10-15.15063 && cd ~/vm/msedge-windows10-15.15063
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-15.15063.txt
$ unzip MSEdge.Win10.RS2.VirtualBox.zip
$ rm msedge-windows10-15.15063.txt MSEdge.Win10.RS2.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).
- **Note:** this release will prompt for password on bootup for the `IEUser` user. Supply the password of `Passw0rd!` to proceed with login.


### MS Edge - Windows 10 Stable (16.16299)
```sh
$ mkdir -p ~/vm/msedge-windows10-16.16299 && cd ~/vm/msedge-windows10-16.16299
$ wget -ci https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/master/vmarchiveset/msedge-windows10-16.16299.txt
$ unzip MSEdge.Win10.VirtualBox.zip
$ rm msedge-windows10-16.16299.txt MSEdge.Win10.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


## Activating images
For Windows **7, 8, 8.1 and 10** images once connected to the Internet you will need to activate the OS trial to give a full 90 days of use. Enter the following from the Command Prompt running as administrator (Start - Right click Command Prompt - Run as administrator):

```
C:\> slmgr /ato
```

After a short delay you should be presented with a dialog telling you your Windows OS has been successfully activated for a 90 day trial.

## Rearming images
For Windows **XP, Vista and 7** images you *may* be able to extend the initial trial usage period once it has expired via the "rearm" process:

- To rearm a Windows XP image, from the command prompt:

	```
	C:\> rundll32.exe syssetup,SetupOobeBnk
	```

- To rearm Windows Vista and 7 images run the following as an administrator from the command prompt:

	```
	C:\> slmgr /rearm
	```

It is not currently possible to rearm the trial period of **Windows 8, 8.1 or 10** images.


## Reference
- https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/
- http://modernievirt.blob.core.windows.net/vhd/release_notes_license_terms_1_5_15.pdf
- https://blog.reybango.com/2013/02/04/making-internet-explorer-testing-easier-with-new-ie-vms/
- API endpoint returning latest Microsoft Virtual Machine builds (thanks to [Antón Molleda](https://twitter.com/molant) for the tip):
	- https://developer.microsoft.com/en-us/microsoft-edge/api/tools/vms/
