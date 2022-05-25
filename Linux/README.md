# Linux | Forensic Imaging | Quickstarts
There are many open-source tools out there to help with forensic imaging.

This section is all about the Linux tools.

## Command list
- `sg_raw` - send arbitrary SCSI or NVMe command to a device
- `dmesg` - print or control the kernel ring buffer
- `blockdev` - call block device ioctls from the command line
- `icat` - Output the contents of a file based on its inode number.
- `exif` - shows EXIF information in JPEG files
- `objdump` - display information from object files
- `fls` - List file and directory names in a disk image. (can display file names of recently deleted files for the directory using the given inode)
- `dd` - convert and copy a file
- `dmidecode` - DMI table decoder.
     > dmidecode is a tool for dumping a computer's DMI (some say SMBIOS) table contents in a human-readable format. This table contains a description of the system's hardware components, as well as other useful pieces of information  such as serial numbers and BIOS revision. Thanks to this table, you can retrieve this information without having to probe for the actual hardware. While this is a good point in terms of report speed and safeness, this also makes the presented information possibly unreliable.
     > 
     > The  DMI table doesn't only describe what the system is currently made of, it also can report the possible evolutions (such as the fastest supported CPU or the maximal amount of memory supported).
     >
     > SMBIOS stands for System Management BIOS, while DMI stands for Desktop Management Interface. Both standards are tightly related and developed by the DMTF (Desktop Management Task Force).
- `lshw` - list hardware
- `lsusb` - list USB devices
- `hdparm` - get/set SATA/IDE device parameters
- `smartctl` - Control and Monitor Utility for SMART Disks
- `mmls` - Display the partition layout of a volume system  (partition tables)
- `mmcat` - Output the contents of a partition to stdout
- `sedutil-cli` - Is a utility to manage self encrypting drives that conform to the Trusted Computing Group (TCG) OPAL 2.0 SSC specification.
- `hddtemp` - Utility to monitor hard drive temperature
- `mt` - Gives subcommands to streaming tape device.
- `nvme` - 
- `df` - report file system disk space usage
- `du` - estimate file space usage
- `gzip`, `gunzip`, `zcat` - compress or expand files
- `ewfverify` - verifies media data stored in EWF files 
- `affinfo` - print information about an AFF file
- `img_stat` - Display details of an image file 
- `dc3dd` - convert and copy a file
- `growisofs` - combined mkisofs frontend/DVD recording program.
- `mkisofs` - create an hybrid ISO9660/JOLIET/HFS filesystem with optional Rock Ridge attributes.
- `blkcat` - Display the contents of file system data unit in a disk image.
- `blkls` - List or output file system data units.
- `fsstat` - Display general details of a file system
- `gpart` - control utility for the disk partitioning GEOM class
- `dcfldd` - enhanced version of dd for forensics and security. Copy a file, converting and formatting according to the options.
- `veracrypt` - Free and open source disk encryption software.
- `udev` - Dynamic device management
- `udevadm` - udev management tool
- `mknod` - make block or character special files

## Setup
### Debian
- `sg3-utils` this includes tools like `sg_raw` (SCSI or NVMe disks)
```bash
sudo apt update
sudo apt install -y sg3-utils exif lshw hddtemp dc3dd
```
> This `apt install` was tested on Kali Linux.

## Linux Kernel and Filesystem
- Everything on Unix/Linux systems is a *file*
    - Each file is of a specific type
        - regular files
        - directories
        - Block devices
        - character devices
        - named pipes
        - hard links
        - soft/symbolic links (similar to Microsoft Windows LNK files)

### Kernel Device Detection
- `/dev` dir stores files that correspond to devices
- `mknod` is the command for creation of devices files
    - It is done automatically
    - Past system: `devfs`
    - `udev` is the program that loads devices (the deamon can be `systemd-udevd`)
    - The Kernel is the one calling `udev`

![](./assets/Linux-storage-stack-diagram_v4.10.png)
*The Linux Storage Stack Diagram (Source: https://www.thomas-krenn.com/en/wiki/Linux_Storage_Stack_Diagram, used under CC Attribution-ShareAlike 3.0 Unported)*

## Commands
## `nvme`

**Resouces:**
- https://nvmexpress.org/open-source-nvme-management-utility-nvme-command-line-interface-nvme-cli/
- https://github.com/linux-nvme/nvme-cli
- https://github.com/linux-nvme

## `df`
To make the output more readable use the `-h` flag.

## `udev`
- Is called by the Kernel
- It creates: 
    - devices (in `/dev`)
    - proper permissions
    - executes setup or removal of scripts and programs
    - sends messages to other deamons via `dbus` maybe others
- You can see it in action with this command: `udevadm monitor`
- You can also get information about a devices associated files/paths: `udevadmin info /dev/<device>`

## `udevadm`
For monitoring devices being removed and added: `udevadm monitor`
