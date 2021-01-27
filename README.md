# Running IE 8/9/10/11/Edge Virtual machines from Microsoft under Linux via VirtualBox

:warning::warning::warning::warning:

**Microsoft have (sadly) removed most (if not all) of these VM images from their public CDN. Repository will remain for historical purposes.**

:warning::warning::warning::warning:

Detailed step-by-step notes for installing the [Microsoft provided Internet Explorer virtual machines](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/) under Linux using VirtualBox.

Tested under Ubuntu 16.04LTS (previously 14.04LTS) with [VirtualBox](https://www.virtualbox.org) version 5.2.

- [General notes](#general-notes)
- [Available images](#available-images)
	- [IE8 - Windows 7](#ie8---windows-7)
	- [IE9 - Windows 7](#ie9---windows-7)
	- [IE10 - Windows 7](#ie10---windows-7)
	- [IE11 - Windows 7](#ie11---windows-7)
	- [IE11 - Windows 8.1](#ie11---windows-81)
	- [MS Edge - Windows 10 Stable (13.10586)](#ms-edge---windows-10-stable-1310586)
	- [MS Edge - Windows 10 Preview (14.14342)](#ms-edge---windows-10-preview-1414342)
	- [MS Edge - Windows 10 Stable (14.14393)](#ms-edge---windows-10-stable-1414393)
	- [MS Edge - Windows 10 Preview (15.14959)](#ms-edge---windows-10-preview-1514959)
	- [MS Edge - Windows 10 Preview (15.15014)](#ms-edge---windows-10-preview-1515014)
	- [MS Edge - Windows 10 Preview (15.15063)](#ms-edge---windows-10-preview-1515063)
	- [MS Edge - Windows 10 Stable (16.16299)](#ms-edge---windows-10-stable-1616299)
	- [MS Edge - Windows 10 Preview (17.17074)](#ms-edge---windows-10-preview-1717074)
	- [MS Edge - Windows 10 Preview (17.17127)](#ms-edge---windows-10-preview-1717127)
	- [MS Edge - Windows 10 Stable (17.17134)](#ms-edge---windows-10-stable-1717134)
- [Activating images](#activating-images)
- [Rearming images](#rearming-images)
- [Reference](#reference)

## General notes

- Download, re-construct and decompress archive image as per each images instructions below.
- From VirtualBox goto `File` -> `Import Appliance...`
- Select the decompressed Open Virtualization Format `ovf` file.
- Review virtual machine name and settings (adjusting to suit if required), then click `Import`.
- Before starting the image, create a snapshot of the current machine state - this will allow you to quickly roll back to a fresh virtual machine once the usage period of the OS expires.
- Images are **32bit** virtual machines *except* for the following, which are **64 bit**:
	- [MS Edge - Windows 10 Stable (13.10586)](#ms-edge---windows-10-stable-1310586)
	- [MS Edge - Windows 10 Preview (14.14342)](#ms-edge---windows-10-preview-1414342)
	- [MS Edge - Windows 10 Stable (14.14393)](#ms-edge---windows-10-stable-1414393)
	- [MS Edge - Windows 10 Preview (15.14959)](#ms-edge---windows-10-preview-1514959)
	- [MS Edge - Windows 10 Preview (15.15014)](#ms-edge---windows-10-preview-1515014)
	- [MS Edge - Windows 10 Preview (15.15063)](#ms-edge---windows-10-preview-1515063)
	- [MS Edge - Windows 10 Stable (16.16299)](#ms-edge---windows-10-stable-1616299)
	- [MS Edge - Windows 10 Preview (17.17074)](#ms-edge---windows-10-preview-1717074)
	- [MS Edge - Windows 10 Preview (17.17127)](#ms-edge---windows-10-preview-1717127)
	- [MS Edge - Windows 10 Stable (17.17134)](#ms-edge---windows-10-stable-1717134)
- You may need to update the images installed **VirtualBox Guest Additions** after VM startup to match that of your VirtualBox version.
- It's a smart idea to keep a clean copy of each `ovf` disk image once the OS usage period ends, to avoid a full image re-download hit.


## Available images

### IE8 - Windows 7
```sh
$ mkdir --parents ~/vm/ie8-windows7 && cd ~/vm/ie8-windows7
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/ie8-windows7.txt
$ unzip IE8.Win7.VirtualBox.zip
$ rm IE8.Win7.VirtualBox.zip
```

- Use the resulting `IE8 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE9 - Windows 7
```sh
$ mkdir --parents ~/vm/ie9-windows7 && cd ~/vm/ie9-windows7
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/ie9-windows7.txt
$ unzip IE9.Win7.VirtualBox.zip
$ rm IE9.Win7.VirtualBox.zip
```

- Use the resulting `IE9 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE10 - Windows 7
```sh
$ mkdir --parents ~/vm/ie10-windows7 && cd ~/vm/ie10-windows7
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/ie10-windows7.txt
$ unzip IE10.Win7.VirtualBox.zip
$ rm IE10.Win7.VirtualBox.zip
```

- Use the resulting `IE10 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 7
```sh
$ mkdir --parents ~/vm/ie11-windows7 && cd ~/vm/ie11-windows7
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/ie11-windows7.txt
$ unzip IE11.Win7.VirtualBox.zip
$ rm IE11.Win7.VirtualBox.zip
```

- Use the resulting `IE11 - Win7.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### IE11 - Windows 8.1
```sh
$ mkdir --parents ~/vm/ie11-windows8.1 && cd ~/vm/ie11-windows8.1
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/ie11-windows8.1.txt
$ unzip IE11.Win81.VirtualBox.zip
$ rm IE11.Win81.VirtualBox.zip
```

- Use the resulting `IE11 - Win8.1.ova` with VirtualBox.
- Recommended 1024MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Stable (13.10586)
```sh
$ mkdir --parents ~/vm/msedge-windows10-13.10586 && cd ~/vm/msedge-windows10-13.10586
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-13.10586.txt
$ unzip MSEdge.Win10TH2.VirtualBox.zip
$ rm msedge-windows10-13.10586.txt MSEdge.Win10TH2.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10TH2.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (14.14342)
```sh
$ mkdir --parents ~/vm/msedge-windows10-14.14342 && cd ~/vm/msedge-windows10-14.14342
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-14.14342.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-14.14342.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_14342.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Stable (14.14393)
```sh
$ mkdir --parents ~/vm/msedge-windows10-14.14393 && cd ~/vm/msedge-windows10-14.14393
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-14.14393.txt
$ unzip MSEdge.Win10_RS1.VirtualBox.zip
$ rm msedge-windows10-14.14393.txt MSEdge.Win10_RS1.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.14959)
```sh
$ mkdir --parents ~/vm/msedge-windows10-15.14959 && cd ~/vm/msedge-windows10-15.14959
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-15.14959.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-15.14959.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.15014)
```sh
$ mkdir --parents ~/vm/msedge-windows10-15.15014 && cd ~/vm/msedge-windows10-15.15014
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-15.15014.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-15.15014.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (15.15063)
```sh
$ mkdir --parents ~/vm/msedge-windows10-15.15063 && cd ~/vm/msedge-windows10-15.15063
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-15.15063.txt
$ unzip MSEdge.Win10.RS2.VirtualBox.zip
$ rm msedge-windows10-15.15063.txt MSEdge.Win10.RS2.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).
- **Note:** this release will prompt for password on bootup for the `IEUser` user. Supply the password of `Passw0rd!` to proceed with login.


### MS Edge - Windows 10 Stable (16.16299)
```sh
$ mkdir --parents ~/vm/msedge-windows10-16.16299 && cd ~/vm/msedge-windows10-16.16299
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-16.16299.txt
$ unzip MSEdge.Win10.VirtualBox.zip
$ rm msedge-windows10-16.16299.txt MSEdge.Win10.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (17.17074)
```sh
$ mkdir --parents ~/vm/msedge-windows10-17.17074 && cd ~/vm/msedge-windows10-17.17074
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-17.17074.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-17.17074.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Preview (17.17127)
```sh
$ mkdir --parents ~/vm/msedge-windows10-17.17127 && cd ~/vm/msedge-windows10-17.17127
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-17.17127.txt
$ unzip MSEdge.Win10_preview.VirtualBox.zip
$ rm msedge-windows10-17.17127.txt MSEdge.Win10_preview.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10_preview.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


### MS Edge - Windows 10 Stable (17.17134)
```sh
$ mkdir --parents ~/vm/msedge-windows10-17.17134 && cd ~/vm/msedge-windows10-17.17134
$ wget --continue --input-file https://github.com/magnetikonline/linuxmicrosoftievirtualmachines/raw/main/vmarchiveset/msedge-windows10-17.17134.txt
$ unzip MSEdge.Win10.VirtualBox.zip
$ rm msedge-windows10-17.17134.txt MSEdge.Win10.VirtualBox.zip
```

- Use the resulting `MSEdge - Win10.ova` with VirtualBox.
- Recommended 2048MB RAM minimum.
- After install you will need to [activate the trial](#activating-images) to gain a full 90 days usage period, after which you may be able to [rearm the image](#rearming-images).


## Activating images
For Windows **7, 8.1 and 10** images once connected to the Internet you will need to activate the OS trial to give a full 90 days of use. Enter the following from the Command Prompt running as administrator (Start - Right click Command Prompt - Run as administrator):

```
C:\> slmgr /ato
```

After a short delay you should be presented with a dialog telling you your Windows OS has been successfully activated for a 90 day trial.

## Rearming images

For Windows **7** images you *may* be able to extend the initial trial usage period once it has expired via the "rearm" process. Enter the following as an administrator from the command prompt:

```
C:\> slmgr /rearm
```

It is not currently possible to rearm the trial period of **Windows 8.1 or 10** images.


## Reference

- https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/linux/
- http://modernievirt.blob.core.windows.net/vhd/release_notes_license_terms_1_5_15.pdf
- https://blog.reybango.com/2013/02/04/making-internet-explorer-testing-easier-with-new-ie-vms/
- API endpoint returning latest Microsoft Virtual Machine builds (thanks to [Antón Molleda](https://twitter.com/molant) for the tip):
	- https://developer.microsoft.com/en-us/microsoft-edge/api/tools/vms/
