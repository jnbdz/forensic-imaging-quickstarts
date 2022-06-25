<img src="../assets/tux-inflated.jpg" alt="Tux" style="width: 255px;" align="right">

# Linux | Forensic Imaging | Quickstarts
There are many open-source tools out there to help with forensic imaging.

This section is all about the Linux tools.

## Setup
### Kali
You can quickly install useful packages for Forensic Tools in Kali: 
```bash
sudo apt install kali-tools-forensics
```
**Source:** https://www.kali.org/tools/kali-meta/#kali-tools-forensics
> **NOTE:** If you click on *Dependencies* you can see all the packages that will be installed.
## Forensic tools
- Sleuth Kit
- dcfldd
- foremost
- [...]
### Comes with *Kali forensics tools*
- [**afflib-tools**](https://packages.debian.org/unstable/afflib-tools) - The Advanced Forensic Format (AFF) is on-disk format for storing computer forensic information. Critical features of AFF include:
    - AFF allows you to store both computer forensic data and associated
   metadata in one or more files.
    - AFF allows files to be digital signed, to provide for
   chain-of-custody and long-term file integrity.
    - AFF allows for forensic disk images to stored encrypted and decrypted on-the-fly for processing. This allows disk images containing privacy sensitive material to be stored on the Internet.
- [**apktool**](https://packages.debian.org/unstable/apktool) -  A tool for reverse engineering 3rd party, closed, binary Android apps. It can decode resources to nearly original form and rebuild them after making some modifications; it makes possible to debug smali code step by step. Also it makes working with an app easier because of project-like file structure and automation of some repetitive tasks like building apk.
- [**autopsy**](https://packages.debian.org/unstable/autopsy) - The Autopsy Forensic Browser is a graphical interface to the command line digital forensic analysis tools in The Sleuth Kit. Together, The Sleuth Kit and Autopsy provide many of the same features as commercial digital forensics tools for the analysis of Windows and UNIX file systems (NTFS, FAT, FFS, EXT2FS, and EXT3FS).
- [**binwalk**](https://packages.debian.org/unstable/binwalk) - Binwalk is a tool for searching a given binary image for embedded files and executable code. Specifically, it is designed for identifying files and code embedded inside of firmware images. Binwalk uses the libmagic library, so it is compatible with magic signatures created for the Unix file utility. Binwalk also includes a custom magic signature file which contains improved signatures for files that are commonly found in firmware images such as compressed/archived files, firmware headers, Linux kernels, bootloaders, filesystems, etc.
- [**bulk-extractor**](https://github.com/simsong/bulk_extractor) or [Kali tools](https://www.kali.org/tools/bulk-extractor/) - bulk_extractor is a C++ program that scans a disk image, a file, or a directory of files and extracts useful information without parsing the file system or file system structures. The results are stored in feature files that can be easily inspected, parsed, or processed with automated tools. bulk_extractor also creates histograms of features that it finds, as features that are more common tend to be more important.
- [**bytecode-viewer**](https://github.com/Konloch/bytecode-viewer) or [Kali tools](https://www.kali.org/tools/bytecode-viewer/)- This package contains Bytecode Viewer (BCV). It is an Advanced Lightweight Java Bytecode Viewer, GUI Java Decompiler, GUI Bytecode Editor, GUI Smali, GUI Baksmali, GUI APK Editor, GUI Dex Editor, GUI APK Decompiler, GUI DEX Decompiler, GUI Procyon Java Decompiler, GUI Krakatau, GUI CFR Java Decompiler, GUI FernFlower Java Decompiler, GUI DEX2Jar, GUI Jar2DEX, GUI Jar-Jar, Hex Viewer, Code Searcher, Debugger and more. There is also a plugin system that will allow you to interact with the loaded classfiles, for example you can write a String deobfuscator, a malicious code searcher, or something else you can think of. You can either use one of the pre-written plugins, or write your own. It supports groovy scripting. Once a plugin is activated, it will execute the plugin with a ClassNode ArrayList of every single class loaded in BCV, this allows the user to handle it completely using ASM.
- [**cabextract**](https://packages.debian.org/unstable/cabextract) - Cabextract is a program which unpacks cabinet (.cab) files, which are a form of archive Microsoft uses to distribute their software and things like Windows Font Packs.
- [**chkrootkit**](https://packages.debian.org/unstable/chkrootkit) - The chkrootkit security scanner searches for signs that the system is infected with a 'rootkit'. Rootkits are a form of malware that seek to exploit security flaws to grant unauthorised access to a computer or its services, generally for malicious purposes.chkrootkit can identify signs of over 70 different rootkits (see the project's website for a list). Please note that an automated tool like chkrootkit can never guarantee a system is uncompromised. Nor does every report always signify a genuine problem: human judgement and further investigation will always be needed to assure the security of your system.
- [**creddump7**](https://packages.debian.org/unstable/creddump7) - This package contains a Python tool to extract various credentials and secrets from Windows registry hives. It's based on the creddump program. Many patches and fixes have been applied by Ronnie Flathers.
- [**dc3dd**](https://packages.debian.org/unstable/dc3dd) - dc3dd is a patched version of GNU dd with added features for computer forensics: 
    - on the fly hashing (md5, sha-1, sha-256, and sha-512)
    - possibility to write errors to a file
    - group errors in the error log
    - pattern wiping
    - progress report
    - possibility to split output
- [**dc3dd**](https://packages.debian.org/unstable/dcfldd) - dcfldd was initially developed at Department of Defense Computer Forensics Lab (DCFL). This tool is based on the dd program with the following additional features: 
    - Hashing on-the-fly: dcfldd can hash the input data as it is being
   transferred, helping to ensure data integrity.
    - Status output: dcfldd can update the user of its progress in terms of the
   amount of data transferred and how much longer operation will take.
    - Flexible disk wipes: dcfldd can be used to wipe disks quickly and with a
   known pattern if desired.
    - Image/wipe verify: dcfldd can verify that a target drive is a bit-for-bit
   match of the specified input file or pattern.
    - Multiple outputs: dcfldd can output to multiple files or disks at the same
   time.
    - Split output: dcfldd can split output to multiple files with more
   configurability than the split command.
    - Piped output and logs: dcfldd can send all its log data and output to
   commands as well as files natively.
    - When dd uses a default block size (bs, ibs, obs) of 512 bytes, dcfldd uses
   32768 bytes (32 KiB) which is HUGELY more efficient.
    - The following options are present in dcfldd but not in dd: ALGORITHMlog:,
   errlog, hash, hashconv, hashformat, hashlog, hashlog:, hashwindow, limit,
   of:, pattern, sizeprobe, split, splitformat, statusinterval, textpattern,
   totalhashformat, verifylog, verifylog:, vf.
- [**ddrescue**](http://www.garloff.de/kurt/linux/ddrescue/) or [Kali tools](https://www.kali.org/tools/ddrescue/) - When your disk has crashed and you try to copy it over to another one, standard Unix tools like cp, cat, and dd will abort on every I/O error, dd_rescue does not. It optimizes copying by using large blocks as long as no errors occur and falls back to smaller blocks. It supports reverse direction copying (to approach a bad spot from the top), sparse copying, preallocating space, splice zerocopy, and bypassing the kernel pagecache with O_DIRECT. dd_rescue provides safe deletion of data by overwriting files (or better partitions/disks) multiple times with fast random numbers. With the ddr_hash plugin, it supports calculating a hash value (such as a sha256sum) or an HMAC during copying.
- [**dumpzilla**](https://www.kali.org/tools/dumpzilla/) - Dumpzilla application is developed in Python 3.x and has as purpose extract all forensic interesting information of Firefox, Iceweasel and Seamonkey browsers to be analyzed. Due to its Python 3.x development, might not work properly in old Python versions, mainly with certain characters. Works under Unix and Windows 32/64 bits systems. Works in command line interface, so information dumps could be redirected by pipes with tools such as grep, awk, cut, sed… Dumpzilla allows one to visualize following sections, search customization and extract certain content.
- [**edb-debugger**](https://www.kali.org/tools/edb-debugger/) [GitHub](https://github.com/eteran/edb-debugger) - edb is a graphical cross platform x86/x86-64 debugger. It was inspired by Ollydbg, but aims to function on x86 and x86-64 as well as multiple OS’s. Linux is the only officially supported platform at the moment, but FreeBSD, OpenBSD, OSX and Windows ports are underway with varying degrees of functionality.
- [**edb-debugger** or **libewf**](https://www.kali.org/tools/libewf/) [GitHub](https://github.com/libyal/libewf-legacy) - Libewf is a library with support for reading and writing the Expert Witness Compression Format (EWF). This library allows you to read media information of EWF files in the SMART (EWF-S01) format and the EnCase (EWF-E01) format. It supports files created by EnCase 1 to 6, linen and FTK Imager. The libewf is useful for forensics investigations. This package contains tools to acquire, verify and export EWF files.
- [**exifprobe**](https://www.kali.org/tools/exifprobe/) [GitHub](https://github.com/hfiguiere/exifprobe) - Exifprobe reads image files produced by digital cameras (including several so-called “raw” file formats) and reports the structure of the files and the auxiliary data and metadata contained within them. In addition to TIFF, JPEG and EXIF, the program understands several formats which may contain “raw” camera data, including MRW, CIFF/CRW, JP2/JPEG2000, RAF, and X3F, as well as most TIFF-derived “raw” formats, including DNG, ORF, CR2, NEF, K25/KDC/DCR and PEF. This program is useful in forensics investigations.
- [**exiv2**](https://www.kali.org/tools/exiv2/) [Official website](https://www.exiv2.org/) - Exiv2 is a C++ library and a command line utility to manage image metadata. It provides fast and easy read and write access to the Exif, IPTC and XMP metadata of images in various formats. Exiv2 command line utility to: 
    - print Exif, IPTC and XMP image metadata in different formats:
        - Exif summary info, interpreted values, or the plain data for each tag
    - set, add and delete Exif, IPTC and XMP image metadata from command line modify commands or command scripts
    - adjust the Exif timestamp (that’s how it all started…)
    - rename Exif image files according to the Exif timestamp
    - extract, insert and delete Exif, IPTC and XMP metadata and JPEG comments
    - extract previews from RAW images and thumbnails from the Exif metadata
    - insert and delete the thumbnail image embedded in the Exif metadata
    - print, set and delete the JPEG comment of JPEG images
    - fix the Exif ISO setting of picture taken with Canon and Nikon cameras
- [**ext3grep**](https://www.kali.org/tools/ext3grep/) [Google Code](https://code.google.com/archive/p/ext3grep/) - ext3grep is a simple tool intended to aid anyone who accidentally deletes a file on an ext3 filesystem, only to find that they wanted it shortly thereafter. This package is useful in forensics investigations.
- [**ext4magic**](https://www.kali.org/tools/ext4magic/) [Official website](http://ext4magic.sf.net/ext4magic_en.html) - ext4magic is a file carver (or file carving). It can be used when recovering from disasters or in digital forensics activities. The deletion of files in ext3/4 filesystems can not be easily reversed. Zero out of the block references in the inodes makes that impossible. Experiences with other programs have proved that is possible restore sufficient information for a recover of many data files, directly from the filesystem journal. ext4magic can extract the information from the journal and restore files in an entire directory tree, if the information in the journal are sufficient. This tool can recover the most file types, with original filename, owner and group, file mode bits and also the old atime/mtime stamps.
- [**extundelete**](https://www.kali.org/tools/extundelete/) [SourceForge](http://extundelete.sourceforge.net/) - extundelete uses the information stored in the partition’s journal to attempt to recover a file that has been deleted. There is no guarantee that any particular file will be able to be undeleted.
- [**fcrackzip**](https://www.kali.org/tools/fcrackzip/) [Homepage](http://oldhome.schmorp.de/marc/fcrackzip.html) - fcrackzip is a fast password cracker partly written in assembler. It is able to crack password protected zip files with brute force or dictionary based attacks, optionally testing with unzip its results. It can also crack cpmask’ed images. This package is useful for pentesters, ethical hackers and forensics experts.
- [**firmware-mod-kit**](https://www.kali.org/tools/firmware-mod-kit/) [GitHub](https://github.com/rampageX/firmware-mod-kit) - The Firmware Mod Kit allows for easy deconstruction and reconstruction of firmware images for various embedded devices. While it primarily targets Linux based routers, it should be compatible with most firmware that makes use of common firmware formats and file systems such as TRX/uImage and SquashFS/CramFS.
- [**foremost**](https://www.kali.org/tools/foremost/) [SourceForge](https://sourceforge.net/projects/foremost/) - Foremost is a forensic program to recover lost files based on their headers, footers, and internal data structures. Foremost can work on image files, such as those generated by dd, Safeback, Encase, etc, or directly on a drive. The headers and footers can be specified by a configuration file or you can use command line switches to specify built-in file types. These built-in types look at the data structures of a given file format allowing for a more reliable and faster recovery.
- [**forensic-artifacts**](https://www.kali.org/tools/forensic-artifacts/) [GitHub](https://www.kali.org/tools/forensic-artifacts/) (`python3-artifacts`) - A free, community-sourced, machine-readable knowledge base of forensic artifacts that the world can use both as an information source and within other tools. This package installs the data files alone, without the Python toolkit.
- [**forensics-colorize**](https://www.kali.org/tools/forensics-colorize/) [GitHub](https://github.com/jessek/colorize) - forensics-colorize is a set of tools to visually compare large files, as filesystem images, creating graphics of them. It is intuitive because the produced graphics provide a quick and perfect sense about the percentage of changes between two files. Comparing large textual files using a simple diff can produce a very big result in lines, causing confusion. On the other hand, diff is improper to compare binary files. This package provides two command line programs: filecompare and colorize. The filecompare command is used to create a special and auxiliary input file for colorize. The colorize command will generate an intuitive graphic that will make easier to perceive the level of changes between the files.
- [**galleta**](https://www.kali.org/tools/galleta/) [SourceForge](http://odessa.sourceforge.net/) - Galleta is a forensics tool that examines the content of cookie files produced by Microsoft Internet Explorer (MSIE). It parses the file and outputs a field separated that can be loaded in a spreadsheet.
- [**gdb**](https://www.kali.org/tools/gdb/) [Homepage](https://www.gnu.org/s/gdb/) - GDB is a source-level debugger, capable of breaking programs at any specific line, displaying variable values, and determining where errors occurred. Currently, gdb supports C, C++, D, Objective-C, Fortran, Java, OpenCL C, Pascal, assembly, Modula-2, Go, and Ada. A must-have for any serious programmer.
- [**gpart**](https://www.kali.org/tools/gpart/) [GitHub](https://www.kali.org/tools/gpart/) - Gpart is a tool which tries to guess the primary partition table of a PC-type disk in case the primary partition table in sector 0 is damaged, incorrect or deleted. It is also good at finding and listing the types, locations, and sizes of inadvertently-deleted partitions, both primary and logical. It gives you the information you need to manually re-create them (using fdisk, cfdisk, sfdisk, etc.). The guessed table can also be written to a file or (if you firmly believe the guessed table is entirely correct) directly to a disk device. Gpart is useful in recovery actions and forensics investigations. Currently supported (guessable) filesystem or partition types:
    - BeOS filesystem type.
    - BtrFS filesystem type.
    - FreeBSD/NetBSD/386BSD disklabel sub-partitioning scheme used on Intel platforms.
    - Linux second extended filesystem (Ext2).
    - MS-DOS FAT12, FAT16 and FAT32 “filesystems”.
    - IBM OS/2 High Performance filesystem.
    - Linux LVM and LVM2 physical volumes.
    - Linux swap partitions (versions 0 and 1).
    - The Minix operating system filesystem type.
    - MS Windows NT/2000 filesystem.
    - QNX 4.x filesystem.
    - The Reiser filesystem (version 3.5.X, X > 11).
    - Sun Solaris on Intel platforms uses a sub-partitioning scheme on PC hard disks similar to the BSD disklabels.
    - Silicon Graphics journaled filesystem for Linux. 
- [**gparted**](https://www.kali.org/tools/gparted/) [Homepage](https://gparted.org/) - GParted uses libparted to detect and manipulate devices and partition tables while several (optional) filesystem tools provide support for filesystems not included in libparted.
    - [**gparted-common**](https://www.kali.org/tools/gparted/) - GParted uses libparted to detect and manipulate devices and partition tables while several (optional) filesystem tools provide support for filesystems not included in libparted. This package contains architecture-independent data, such as documentation and help, icons, and application metadata.
- [**grokevt**](https://www.kali.org/tools/grokevt/) [Homepage](http://projects.sentinelchicken.org/grokevt/)- GrokEVT is a collection of scripts built for reading Microsoft Windows NT/2000/XP/2003 event log files. Currently the scripts work together on one or more mounted Microsoft Windows partitions to extract all information needed (registry entries, message templates, and log files) to convert the logs to a human-readable format. This program is useful in forensics investigations.
- [**guymager**](https://www.kali.org/tools/guymager/) [Sourceforge](http://guymager.sourceforge.net/) - The forensic imager contained in this package, guymager, was designed to support different image file formats, to be most user-friendly and to run really fast. It has a high speed multi-threaded engine using parallel compression for best performance on multi-processor and hyper-threading machines.
- [**hashdeep**](https://www.kali.org/tools/hashdeep/) [Homepage](http://md5deep.sf.net/) - hashdeep is a set of tools to compute MD5, SHA1, SHA256, tiger and whirlpool hashsums of arbitrary number of files recursively. The main hashdeep features are:
    - It can compare those hashsums with a list of known hashes;
    - The tools can display those that match the list or those that does not match;
    - It can display a time estimation when processing large files.
    - It can do piecewise hashing (hash input files in arbitrary sized blocks).
- [**inetsim**](https://www.kali.org/tools/inetsim/) [Homepage](https://www.inetsim.org/index.html) - (Not really for forensic imaging (more networking)) INetSim is a software suite for simulating common internet services in a lab environment, e.g. for analyzing the network behaviour of unknown malware samples. INetSim supports simulation of the following services: HTTP, SMTP, POP3, DNS, FTP, NTP, TFTP, IRC, Ident, Finger, Syslog, ‘Small servers’ (Daytime, Time, Echo, Chargen, Discard, Quotd). Additional features: 
    - Faketime
    - Connection redirection
    - Detailed logging and reports
    - TLS/SSL support for several services
- [**jadx**](https://www.kali.org/tools/jadx/) [GitHub](https://github.com/skylot/jadx) - This package contains a Dex to Java decompiler. It contains a command line and GUI tools for produce Java source code from Android Dex and Apk files. Main features: - decompile Dalvik bytecode to java classes from APK, dex, aar and zip files - decode AndroidManifest.xml and other resources from resources.arsc - deobfuscator included. jadx-gui features: - view decompiled code with highlighted syntax - jump to declaration - find usage - full text search.
- [**javasnoop**](https://www.kali.org/tools/javasnoop/) [Google Code](https://code.google.com/p/javasnoop/) - Normally, without access to the original source code, testing the security of a Java client is unpredictable at best and unrealistic at worst. With access the original source, you can run a simple Java program and attach a debugger to it remotely, stepping through code and changing variables where needed. Doing the same with an applet is a little bit more difficult. JavaSnoop attempts to solve this problem by allowing you attach to an existing process (like a debugger) and instantly begin tampering with method calls, run custom code, or just watch what’s happening on the system.
- [**hivex**]() (libhivex-bin) [Homepage](http://libguestfs.org/) - libhivex is a self-contained library for reading and writing Windows Registry “hive” binary files. This package contains a few command line programs that utilize libhivex.
- [**lime-forensics**](https://packages.debian.org/sid/lime-forensics-dkms) (No Kali link I could find) - LiME (Linux Memory Extractor, formerly DMD) is a Loadable Kernel Module (LKM), which allows the acquisition of volatile memory (RAM) from Linux and Linux-based devices, such as those powered by Android. In others words, you can use it to get a memory image from a machine. The tool supports acquiring memory either to the file system of the device or over the network. LiME is unique in that it is the first tool that allows full memory captures from Android devices. It also minimizes its interaction between user and kernel space processes during acquisition. It will produce memory captures that are more forensically sound than those of other tools designed for Linux memory acquisition. The dump format provided as "lime" is fully compatible with volatility framework. This package provides the source code for the lime-forensics kernel modules to be build with dkms. Kernel source or headers are required to compile these modules.
- [**lvm2**](https://www.kali.org/tools/lvm2/) [Homepage](https://sourceware.org/lvm2/) - The Linux Kernel Device Mapper is the LVM (Linux Logical Volume Management) Team’s implementation of a minimalistic kernel-space driver that handles volume management, while keeping knowledge of the underlying device layout in user-space. This makes it useful for not only LVM, but software raid, and other drivers that create “virtual” block devices. This package contains a daemon to monitor events of devmapper devices.
- [**lynis**](https://www.kali.org/tools/lynis/) [Homepage](https://cisofy.com/lynis/) (not really for forensic imaging) - Lynis is an auditing tool for hardening GNU/Linux and Unix based systems. It scans the system configuration and creates an overview of system information and security issues usable by professional auditors. It can assist in automated audits. Lynis can be used in addition to other software, like security scanners, system benchmarking and fine-tuning tools.
- [**mac-robber**](https://www.kali.org/tools/mac-robber/) [Homepage](https://www.sleuthkit.org/mac-robber) - mac-robber is a digital investigation tool (digital forensics) that collects metadata from allocated files in a mounted filesystem. This is useful during incident response when analyzing a live system or when analyzing a dead system in a lab. The data can be used by the mactime tool in The Sleuth Kit (TSK or SleuthKit only) to make a timeline of file activity. The mac-robber tool is based on the grave-robber tool from TCT (The Coroners Toolkit). mac-robber requires that the filesystem be mounted by the operating system, unlike the tools in The Sleuth Kit that process the filesystem themselves. Therefore, mac-robber will not collect data from deleted files or files that have been hidden by rootkits. mac-robber will also modify the Access times on directories that are mounted with write permissions. mac-robber is useful when dealing with a filesystem that is not supported by The Sleuth Kit or other filesystem analysis tools. You can run mac-robber on an obscure, suspect UNIX filesystem that has been mounted read-only on a trusted system.
- [**magicrescue**](https://www.kali.org/tools/magicrescue/) [GitHub](https://github.com/jbj/magicrescue) - Magic Rescue scans a block device for file types it knows how to recover and calls an external program to extract them. It looks at “magic bytes” (file patterns) in file contents, so it can be used both as an undelete utility and for recovering a corrupted drive or partition. As long as the file data is there, it will find it. Magic Rescue uses files called ‘recipes’. These files have strings and commands to identify and extract data from devices or forensics images. So, you can write your own recipes. Currently, there are the following recipes: avi, canon-cr2, elf, flac, gpl, gzip, jpeg-exif, jpeg-jfif, mbox, mbox-mozilla-inbox, mbox-mozilla-sent, mp3-id3v1, mp3-id3v2, msoffice, nikon-raw, perl, png, ppm, sqlite and zip. This package provides magicrescue, dupemap and magicsort commands. magicrescue is a carver and is useful in forensics investigations.
- [**md5deep**](https://www.kali.org/tools/hashdeep/) [Homepage](http://md5deep.sf.net/) - Compute and compare MD5 message digests.
- [**mdbtools**](https://www.kali.org/tools/mdbtools/) [GitHub](https://github.com/mdbtools/mdbtools) - These are various tools for manipulating JET / MS Access database (MDB) files:
    - utils - provides command line utilities to list tables, export schema, and data, show file versions, and other useful stuff.
    - mdb-sql - a command line SQL tool that allows one to type SQL queries and get results.
- [**memdump**](https://www.kali.org/tools/memdump/) [Homepage](http://www.porcupine.org/forensics/tct.html) - Program which dumps system memory to the standard output stream, skipping over holes in memory maps. By default, the program dumps the contents of physical memory. This program will not work if CONFIG_STRICT_DEVMEM is enabled in kernel. Since 2.6 version, several kernels are enabling this option by default. memdump is useful in security tests and forensics investigations.
- [**metacam**](https://www.kali.org/tools/metacam/) [Homepage](http://www.cheeseplant.org/~daniel/pages/metacam.html) - EXIF (Exchangeable Image File Format) is a standard for storing interchange information in image files, especially those using JPEG compression. Most digital cameras, including mobile phones, now use the EXIF format. The format is part of the DCF standard created by JEIDA to encourage the interoperability between imaging devices. In addition to the standard EXIF fields, MetaCam also supports vendor-specific extensions from Nikon, Olympus, Canon and Casio. This program is useful in forensics investigations.
- [**missidentify**](https://www.kali.org/tools/missidentify/) [Homepage](http://missidentify.sf.net/) - Miss Identify (missidentify) is a program to find MS Windows type win32 applications. By default, it displays the filename of any executable that does not have an extension, as exe, dll, com, sys, cpl, hxs, hxi, olb, rll or tlb. It can also display all the executables regardless the extension. Miss Identify is useful in forensics investigations.
- [**myrescue**](https://www.kali.org/tools/myrescue/) [Homepage](http://myrescue.sf.net/) - myrescue is a program to rescue the still-readable data from a damaged harddisk, CD-ROM, DVD, flash drives, etc. It is similar in purpose to dd_rescue (or ddrescue), but it tries to quickly get out of damaged areas to first handle the not yet damaged part of the disk and return later. This package is useful to recover data from any media and for forensics investigations.
- [**nasm**](https://www.kali.org/tools/nasm/) [Homepage](http://www.nasm.us/) - Netwide Assembler. NASM will currently output flat-form binary files, a.out, COFF and ELF Unix object files, and Microsoft 16-bit DOS and Win32 object files. Also included is NDISASM, a prototype x86 binary-file disassembler which uses the same instruction table as NASM. NASM is released under the GNU Lesser General Public License (LGPL).
- [**nasty**](https://www.kali.org/tools/nasty/) [Homepage](http://www.vanheusden.com/nasty/) - Nasty is a program that helps you to recover the passphrase of your PGP or GPG-key in case you forget or lost it. The following features will make things easier:
    - set minimum/maximum length of the passphrase
    - incremental mode, random mode or reads a file for guessing
    - charset filter
- [**ollydbg**](https://www.kali.org/tools/ollydbg/) [Homepage](http://www.ollydbg.de/) (More for SRE) - OllyDbg is a 32-bit assembler level analysing debugger for Microsoft Windows. Emphasis on binary code analysis makes it particularly useful in cases where source is unavailable.
- [**p7zip**](https://www.kali.org/tools/p7zip/) [SourceForge](http://p7zip.sourceforge.net/) - p7zip is the Unix command-line port of 7-Zip, a file archiver that handles the 7z format which features very high compression ratios. p7zip provides (p7zip can be used with popular compression interfaces (such as File Roller or Nautilus). Another package, p7zip-full, provides 7z and 7za which support more compression formats.):
    - /usr/bin/7zr a standalone minimal version of the 7-zip tool that only handles 7z, LZMA and XZ archives. 7z compression is 30-50% better than ZIP compression.
    - /usr/bin/p7zip a gzip-like wrapper around 7zr.
- [**parted**](https://www.kali.org/tools/parted/) [Homepage](https://www.gnu.org/software/parted) - GNU Parted is a program that allows you to create, destroy, resize, move, and copy disk partitions. This is useful for creating space for new operating systems, reorganizing disk usage, and copying data to new hard disks. This package contains the binary and manual page. Further documentation is available in parted-doc. Parted currently supports DOS, Mac, Sun, BSD, GPT, MIPS, and PC98 partitioning formats, as well as a “loop” (raw disk) type which allows use on RAID/LVM. It can detect and remove ASFS/AFFS/APFS, Btrfs, ext2/3/4, FAT16/32, HFS, JFS, linux-swap, UFS, XFS, and ZFS file systems. Parted also has the ability to create and modify file systems of some of these types, but using it to perform file system operations is now deprecated. The nature of this software means that any bugs could cause massive data loss. While there are no such bugs known at the moment, they could exist, so please back up all important files before running it, and do so at your own risk.
- [**pasco**](https://www.kali.org/tools/pasco/) [Homepage](https://sf.net/projects/odessa) - Pasco is a forensic tool that examines the content of cache files (index.dat) produced by Microsoft Internet Explorer. It parses the file and outputs a field separated that can be loaded in a spreadsheet. This package is useful in forensics investigations.
- [**pdf-parser**](https://www.kali.org/tools/pdf-parser/) [Homepage](https://blog.didierstevens.com/programs/pdf-tools/) - This tool will parse a PDF document to identify the fundamental elements used in the analyzed file. It will not render a PDF document.
- [**pdfid**](https://www.kali.org/tools/pdfid/) [Homepage](https://blog.didierstevens.com/programs/pdf-tools/) - This tool is not a PDF parser, but it will scan a file to look for certain PDF keywords, allowing you to identify PDF documents that contain (for example) JavaScript or execute an action when opened. PDFiD will also handle name obfuscation.
- [**pev**](https://www.kali.org/tools/pev/) [SourceForge](http://pev.sourceforge.net/) - pev is a tool to get information of PE32/PE32+ executables (EXE, DLL, OCX etc) like headers, sections, resources and more.
- [**plaso**](https://www.kali.org/tools/plaso/) [GitHub](https://github.com/log2timeline/plaso) - Plaso (plaso langar að safna öllu) is the Python based back-end engine used by tools such as log2timeline for automatic creation of a super timelines. The goal of log2timeline (and thus plaso) is to provide a single tool that can parse various log files and forensic artifacts from computers and related systems, such as network equipment to produce a single correlated timeline. This timeline can then be easily analysed by forensic investigators/analysts, speeding up investigations by correlating the vast amount of information found on an average computer system.
- [**polenum**](https://www.kali.org/tools/polenum/) [GitHub](https://github.com/Wh1t3Fox/polenum/) - polenum is a Python script which uses the Impacket Library from CORE Security Technologies to extract the password policy information from a windows machine. This allows a non-windows (Linux, Mac OSX, BSD etc..) user to query the password policy of a remote windows box without the need to have access to a windows machine.
- [**pst-utils**](https://www.kali.org/tools/libpst/) [Homepage](https://www.five-ten-sg.com/libpst/) - This package contains tools based on libpst to read data from Microsoft Outlook PST files.
    - readpst - export data from PST files to a variety of formats, including mbox, MH and KMail. Other packages like mb2md are available for subsequent conversions to Maildir and other formats.
    - lspst - list data in PST files.
    - pst2ldif - extract contacts from a PST file and prepare them for input in LDAP
    - pst2dii - export data from PST files to Summation dii load file format
- [**capstone**](https://www.kali.org/tools/capstone/) [Homepage](https://www.capstone-engine.org/) - Capstone is a lightweight multi-platform, multi-architecture disassembly framework. This package contains cstool, a command-line tool to disassemble hexadecimal strings.
- [**dfdatetime**](https://www.kali.org/tools/dfdatetime/) [GitHub](https://github.com/log2timeline/dfdatetime) - dfDateTime, or Digital Forensics date and time, provides date and time objects to preserve accuracy and precision.
- [**dfvfs**](https://www.kali.org/tools/dfvfs/) [GitHub](https://github.com/log2timeline/dfvfs) - The Digital Forensics Virtual File System, provides read-only access to file-system objects from various storage media types and file formats. The goal of dfVFS is to provide a generic interface for accessing file-system objects, for which it uses several back-ends that provide the actual implementation of the various storage media types, volume systems and file systems.
- [**dfwinreg**](https://www.kali.org/tools/dfwinreg/) [GitHub](https://github.com/log2timeline/dfwinreg) - dfWinReg, or Digital Forensics Windows Registry, provides read-only access to Windows Registry objects. The goal of dfWinReg is to provide a generic interface for accessing Windows Registry objects that resembles the Registry key hierarchy as seen on a live Windows system. This package contains the library for Python 3.
- [**distorm3**](https://www.kali.org/tools/distorm3/) [GitHub](https://github.com/gdabah/distorm) - diStorm3 is a binary stream disassembler library project. With diStorm3, no more parsing strings is needed. diStorm3 is really a decomposer, which means it takes an instruction and returns a binary structure which describes it rather than static text. This is great for advanced binary code analysis. This package provides the Python3 bindings.
- [**radare2**](https://www.kali.org/tools/radare2/) [Homepage](https://www.radare.org/) - The project aims to create a complete, portable, multi-architecture, unix-like toolchain for reverse engineering. It is composed by an hexadecimal editor (radare) with a wrapped IO layer supporting multiple backends for local/remote files, debugger (OS X, BSD, Linux, W32), stream analyzer, assembler/disassembler (rasm) for x86, ARM, PPC, m68k, Java, MSIL, SPARC, code analysis modules and scripting facilities. A bindiffer named radiff, base converter (rax), shellcode development helper (rasc), a binary information extractor supporting PE, mach0, ELF, class, etc. named rabin, and a block-based hash utility called rahash. This package provides the libraries from radare2.
- [**radare2-cutter**](https://www.kali.org/tools/radare2-cutter/) [Homepage](https://cutter.re/) - Cutter is a Qt based GUI for reverse engineering binaries, which makes use of the radare2 framework. Advanced users are expected to use the radare2 CLI tools instead, which are much more powerful.
- [**recoverdm**](https://www.kali.org/tools/recoverdm/) [Homepage](https://www.vanheusden.com/recoverdm) - recoverdm recover disks with bad sectors. You can recover files as well complete devices. In case it finds sectors which simply cannot be recovered, it writes an empty sector to the output file and continues. When recovering a CD or a DVD and the program cannot read the sector in “normal mode”, then the program will try to read the sector in “RAW mode” (without error-checking etc.). This toolkit also has a utility called ‘mergebad’ which merges multiple images into one. This package is useful in forensics investigations.
- [**recoverjpeg**](https://www.kali.org/tools/recoverjpeg/) [Homepage](https://www.rfc1149.net/devel/recoverjpeg) - recoverjpeg tries to recover JFIF (JPEG) pictures and MOV movies from a peripheral. This may be useful if you mistakenly overwrite a partition or if a device such as a digital camera memory card is bogus. This package provides these executables: recoverjpeg, recovermov, remove-duplicates and sort-pictures. The remove-duplicates is useful to remove duplicate files found. sort-pictures can be used to sort pictures according to exif date. This package acts as a carver (data carving) and is useful in forensics investigations.
- [**reglookup**](https://www.kali.org/tools/reglookup/) [Homepage](http://projects.sentinelchicken.org/reglookup/) - RegLookup is a system to direct analysis of Windows NT-based registry files providing command line tools, a C API, and a Python module for accessing registry data structures. The project has a focus on providing tools for digital forensics investigations (though is useful for many purposes), and includes algorithms for retrieving deleted data structures from registry hives. Currently the program allows one to read an entire registry and output it in a (mostly) standardized, quoted format. It also provides features for filtering of results based on registry path and data type. The package provides the following commands: reglookup, reglookup-recover and reglookup-timeline.
- [**regripper**](https://www.kali.org/tools/regripper/) [Google code](https://code.google.com/p/regripper/) - RegRipper is an open source tool, written in Perl, for extracting/parsing information (keys, values, data) from the Registry and presenting it for analysis. RegRipper consists of two basic tools, both of which provide similar capability. The RegRipper GUI allows the analyst to select a hive to parse, an output file for the results, and a profile (list of plugins) to run against the hive. When the analyst launches the tool against the hive, the results go to the file that the analyst designated. If the analyst chooses to parse the System hive, they might also choose to send the results to system.txt. The GUI tool will also create a log of it’s activity in the same directory as the output file, using the same file name but using the .log extension (i.e., if the output is written to system.txt, the log will be written to system.log).
- [**rephrase**](https://www.kali.org/tools/rephrase/) [Homepage](https://www.roguedaemon.net/rephrase/) - If you can nearly remember your GnuPG passphrase - but not quite - then Rephrase may be able to help. Tell Rephrase the parts of the passphrase you know, and any number of alternatives for the parts you’re not sure about; and Rephrase will try all the alternatives, in all possible combinations, and tell you which combination (if any) gives you the correct passphrase.
- [**rifiuti**](https://www.kali.org/tools/rifiuti/) [Homepage](https://sf.net/projects/odessa) - Rifiuti is a tool to examine the INFO2 files. The INFO2 file gives meta information about the files found in the MS Windows recycle bin. This package is useful in forensics investigations.
- [**rifiuti2**](https://www.kali.org/tools/rifiuti2/) [Homepage](https://abelcheung.github.io/rifiuti2) - Rifiuti2 analyses recycle bin files from Windows. Analysis of Windows recycle bin is usually carried out during Windows computer forensics. Rifiuti2 can extract file deletion time, original path and size of deleted files and whether the deleted files have been moved out from the recycle bin since they are trashed. Rifiuti2 is a rewrite of rifiuti, which is originally written for identical purpose. Rifiuti2 is designed to be portable and runs on command line environment. Two programs rifiuti and rifiuti-vista are chosen depending on relevant Windows recycle bin format. Then it was extended to cover more functionalities, such as:
    - Handles recycle bin up to Windows 10;
    - Handles ancient Windows like 95, NT4 and ME;
    - Supports all localized versions of Windows - both Unicode-based ones and legacy ones (using ANSI code page);
    - Supports output in XML format as well as original tab-delimited text.
- [**rkhunter**](https://www.kali.org/tools/rkhunter/) [Homepage](http://rkhunter.sourceforge.net/) - Rootkit Hunter scans systems for known and unknown rootkits, backdoors, sniffers and exploits. Using rkhunter alone does not guarantee that a system is not compromised. Running additional tests, such as chkrootkit, is recommended. It checks for:
    - SHA256 hash changes;
    - files commonly created by rootkits;
    - executables with anomalous file permissions;
    - suspicious strings in kernel modules;
    - hidden files in system directories; and can optionally scan within files.
- [**rsakeyfind**](https://www.kali.org/tools/rsakeyfind/) [Homepage](https://citp.princeton.edu/our-work/memory/code/) - rsakeyfind is a tool that locates BER-encoded RSA private keys in MEMORY-IMAGE. If a MODULUS-FILE is specified, it will locate private and public keys matching the hex-encoded modulus read from this file. This package is useful to several activities, as forensics investigations.
- [**safecopy**](https://www.kali.org/tools/safecopy/) [Homepage](http://safecopy.sf.net/) - Safecopy tries to get as much data from SOURCE as possible, even resorting to device specific low level operations if applicable. This is achieved by identifying problematic or damaged areas, skipping over them and continuing reading afterwards. The corresponding area in the destination file is either skipped (on initial creation that means padded with zeros) or deliberately filled with a recognizable pattern to later find affected files on a corrupted device. The work is similar to ddrescue, generating an image of the original media. This media can be floppy disks, harddisk partitions, CDs, DVDs, tape devices, where other tools like dd would fail due to I/O errors. Safecopy uses an incremental algorithm to identify the exact beginning and end of bad areas, allowing the user to trade minimum accesses to bad areas for thorough data resurrection. Multiple passes over the same file are possible, to first retrieve as much data from a device as possible with minimum harm, and then trying to retrieve some of the remaining data with increasingly aggressive read attempts. Safecopy includes a low level I/O layer to read CDROM disks in raw mode, and issue device resets and other helpful low level operations on a number of other device classes. Safecopy is useful in forensics investigations and disaster recovery.
- [**samdump2**](https://www.kali.org/tools/samdump2/) [Homepage](http://ophcrack.sourceforge.net/) - This tool is designed to dump Windows 2k/NT/XP password hashes from a SAM file, using the syskey bootkey from the system hive. This package also provides the functionality of bkhive, which recovers the syskey bootkey from a Windows NT/2K/XP system hive. Syskey is a Windows feature that adds an additional encryption layer to the password hashes stored in the SAM database.
- [**scalpel**](https://www.kali.org/tools/scalpel/) [Homepage](http://www.digitalforensicssolutions.com/Scalpel) - scalpel is a fast file carver that reads a database of header and footer definitions and extracts matching files from a set of image files or raw device files. scalpel is filesystem-independent and will carve files from FAT16, FAT32, exFAT, NTFS, Ext2, Ext3, Ext4, JFS, XFS, ReiserFS, raw partitions, etc. scalpel is a complete rewrite of the Foremost 0.69 file carver and is useful for both digital forensics investigations and file recovery.
- [**scrounge-ntfs**](https://www.kali.org/tools/scrounge-ntfs/) [Homepage](http://thewalter.net/stef/software/scrounge/) - Scrounge NTFS is a data recovery program for NTFS filesystems. It reads each block of the hard disk and try to rebuild the original filesystem tree into a directory. This package is useful in forensics investigations.
- [**sleuthkit**](https://www.kali.org/tools/sleuthkit/) [Homepage](http://www.sleuthkit.org/sleuthkit) - The Sleuth Kit, also known as TSK, is a collection of UNIX-based command line file and volume system forensic analysis tools. The filesystem tools allow you to examine filesystems of a suspect computer in a non-intrusive fashion. Because the tools do not rely on the operating system to process the filesystems, deleted and hidden content is shown. The volume system (media management) tools allow you to examine the layout of disks and other media. You can also recover deleted files, get information stored in slack spaces, examine filesystems journal, see partitions layout on disks or images etc. But is very important clarify that the TSK acts over the current filesystem only. The Sleuth Kit supports DOS partitions, BSD partitions (disk labels), Mac partitions, Sun slices (Volume Table of Contents), and GPT disks. With these tools, you can identify where partitions are located and extract them so that they can be analyzed with filesystem analysis tools. Currently, TSK supports several filesystems, as NTFS, FAT, exFAT, HFS+, Ext3, Ext4, UFS and YAFFS2. This package contains the set of command line tools in The Sleuth Kit.
- [**smali**](https://www.kali.org/tools/smali/) [GitHub](https://www.kali.org/tools/smali/) - smali/baksmali is an assembler/disassembler for the dex format used by dalvik, Android’s Java VM implementation. The syntax is loosely based on Jasmin’s/dedexer’s syntax, and supports the full functionality of the dex format (annotations, debug info, line info, etc.)
- [**ssdeep**](https://www.kali.org/tools/ssdeep/) []() - ssdeep is a tool for recursive computing and matching of Context Triggered Piecewise Hashing (aka Fuzzy Hashing). Fuzzy hashing is a method for comparing similar but not identical files. This tool can be used to compare files like regular hashing does (like md5sum or sha1sum) but it will find similar files with little differences. For example, it can be used to identify modified versions of known files even if data has been inserted, modified, or deleted in the new files. This package is useful in forensics investigations.
- [**tcpdump**](https://www.kali.org/tools/tcpdump/) [Homepage](https://www.tcpdump.org/) - This program allows you to dump the traffic on a network. tcpdump is able to examine IPv4, ICMPv4, IPv6, ICMPv6, UDP, TCP, SNMP, AFS BGP, RIP, PIM, DVMRP, IGMP, SMB, OSPF, NFS and many other packet types. It can be used to print out the headers of packets on a network interface, filter packets that match a certain expression. You can use this tool to track down network problems, to detect attacks or to monitor network activities.
- [**tcpflow**](https://www.kali.org/tools/tcpflow/) [GitHub](https://github.com/simsong/tcpflow) - This program allows you to dump the traffic on a network. tcpdump is able to examine IPv4, ICMPv4, IPv6, ICMPv6, UDP, TCP, SNMP, AFS BGP, RIP, PIM, DVMRP, IGMP, SMB, OSPF, NFS and many other packet types. It can be used to print out the headers of packets on a network interface, filter packets that match a certain expression. You can use this tool to track down network problems, to detect attacks or to monitor network activities.
- [**tcpick**](https://www.kali.org/tools/tcpick/) [Homepage](http://tcpick.sourceforge.net/) - This libpcap-based textmode sniffer can:
    - track, reassemble and reorder TCP streams
    - save the captured flows in different files or display them in the terminal
    - display all the stream on the terminal with different display modes like hexdump, hexdump + ascii, only printable characters, raw mode, colorized mode …
    - handle several network interface types, including ethernet cards and PPP interfaces
- [**tcpreplay**](https://www.kali.org/tools/tcpreplay/) [Homepage](http://tcpreplay.appneta.com/) - Tcpreplay is aimed at testing the performance of a NIDS by replaying real background network traffic in which to hide attacks. Tcpreplay allows you to control the speed at which the traffic is replayed, and can replay arbitrary tcpdump traces. Unlike programmatically-generated artificial traffic which doesn’t exercise the application/protocol inspection that a NIDS performs, and doesn’t reproduce the real-world anomalies that appear on production networks (asymmetric routes, traffic bursts/lulls, fragmentation, retransmissions, etc.), tcpreplay allows for exact replication of real traffic seen on real networks. It included the following executables tcpprep, tcprewrite, tcpreplay-edit, tcpbridge and pcap based captures are possible.
- [**truecrack**](https://www.kali.org/tools/truecrack/) [GitHub](https://github.com/lvaccaro/truecrack) - TrueCrack is a bruteforce password cracker for TrueCrypt (Copyright) volume. It is optimazed with Nvidia Cuda technology. It works with PBKDF2 (defined in PKCS5 v2.0) based on RIPEMD160 Key derivation function and XTS block cipher mode of operation used for hard disk encryption based on AES.
- [**undbx**](https://www.kali.org/tools/undbx/) [GitHub](https://github.com/ZungBang/undbx) - UnDBX is a tool to extract, recover and undelete e-mail messages from MS Outlook Express .dbx files (or similar e-mail programs in MS Windows). Corrupted .dbx files can be parsed to try to recover messages from it. It can also try to undelete messages, not only from Deleted Items but also from fragments of deleted messages that were not overwritten. UnDBX is useful in forensics investigations.
- [**unhide**](https://www.kali.org/tools/unhide/) [Homepage](http://www.unhide-forensics.info/) - Unhide is a forensic tool to find processes and TCP/UDP ports hidden by rootkits, Linux kernel modules or by other techniques. It includes two utilities: unhide and unhide-tcp. unhide-tcp identifies TCP/UDP ports that are listening but are not listed in /bin/netstat through brute forcing of all TCP/UDP ports available. This package can be used by rkhunter in its daily scans. This package is useful for network security checks, in addition to forensics investigations. unhide detects hidden processes using the following six techniques:
    - Compare /proc vs /bin/ps output
    - Compare info gathered from /bin/ps with info gathered by walking thru the procfs.
    - Compare info gathered from /bin/ps with info gathered from syscalls (syscall scanning).
    - Full PIDs space occupation (PIDs bruteforcing)
    - Reverse search, verify that all thread seen by ps are also seen by the kernel (/bin/ps output vs /proc, procfs walking and syscall)
    - Quick compare /proc, procfs walking and syscall vs /bin/ps output
- [**unrar-nonfree**](https://www.kali.org/tools/unrar-nonfree/) [Homepage](https://www.rarlab.com/) - Unrar can extract files from .rar archives. If you want to create .rar archives, install package rar.
- [**upx-ucl**](https://www.kali.org/tools/upx-ucl/) [Homepage](https://upx.github.io/) - UPX is an advanced executable file compressor. UPX will typically reduce the file size of programs and DLLs by around 50%-70%, thus reducing disk space, network load times, download times etc. The current version can compress executables for DOS, Linux/ELF (i386, amd64, ppc32) and some other files for different OS. NOTE: This package is based on the UCL library, which is licensed under GPL.
- [**vinetto**](https://www.kali.org/tools/vinetto/) [GitHub](https://github.com/AtesComp/Vinetto) - vinetto is a console program to extract thumbnail pictures and their metadata from Thumbs.db files, that are generated under Microsoft Windows. vinetto can help \*nix-based forensics investigators to:
    - easily preview thumbnails of deleted pictures on Windows systems;
    - obtain information (dates, path, …) about deleted pictures.
- [**wce**](https://www.kali.org/tools/wce/) [Homepage](http://www.ampliasecurity.com/research.html) - Windows Credentials Editor (WCE) v1.3beta allows you to: NTLM authentication:
    - List logon sessions and add, change, list and delete associated credentials (e.g.: LM/NT hashes)
    - Perform pass-the-hash on Windows natively
    - Obtain NT/LM hashes from memory (from interactive logons, services, remote desktop connections, etc.) which can be used to authenticate to other systems. WCE can perform this task without injecting code, just by reading and decrypting information stored in Windows internal memory structures. It also has the capability to automatically switch to code injection when the aforementioned method cannot be performed.
- [**wireshark**](https://www.kali.org/tools/wireshark/) [Homepage](https://www.wireshark.org/) - Wireshark is a network “sniffer” - a tool that captures and analyzes packets off the wire. Wireshark can decode too many protocols to list here.
- [**xmount**](https://www.kali.org/tools/xmount/) [Homepage](https://www.pinguin.lu/) - xmount can be used to boot forensic disk images with QEMU, KVM, VirtualBox, VMware, or the like, since it supports virtual write access with redirection to a cache file. xmount converts between multiple input and output disk image types on the fly, using FUSE (Filesystem in Userspace) to create a virtual file system representing the input image. The virtual representation can be in raw DD, DMG, VirtualBox VDI format, Microsoft VHD format, or VMware VMDK format; input images can be raw DD, EWF (Expert Witness Compression Format), or AFF (Advanced Forensic Format) files.
- [**xplico**](https://www.kali.org/tools/xplico/) [Homepage](http://www.xplico.org/) - The goal of Xplico is extract from an internet traffic capture the applications data contained. For example, from a pcap file Xplico extracts each email (POP, IMAP, and SMTP protocols), all HTTP contents, each VoIP call (SIP, MGCP, H323), FTP, TFTP, and so on. Xplico is not a network protocol analyzer.
- [**yara**](https://www.kali.org/tools/yara/) [Homepage](https://virustotal.github.io/yara/) - YARA is a tool aimed at helping malware researchers to identify and classify malware samples. With YARA, it is possible to create descriptions of malware families based on textual or binary patterns contained in samples of those families. Each description consists of a set of strings and a Boolean expression which determines its logic. Complex and powerful rules can be created by using binary strings with wild-cards, case-insensitive text strings, special operators, regular expressions and many other features.

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

## Storage Devices
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
    - `/dev` raw disk device files have a naming convention: 
        - SATA & SCSI: *sd**
        - IDE: *hd**
        - RAID arrays: *md**
        - NVME drives: <em>nvme&#42;n&#42;</em>
        - [...]
    - Other devices of note: 
        - `/dev/null` - discards any data written to it
        - `/dev/zero` - steady stream of zeros
        - `/dev/random` - stream of random data
        - `/dev/st` - normally this is how tape drives start
        - `/dev/dvd` - media DVD
        - `/dev/cdrom` - media CD
        - `/dev/sr*` - majority of the time they are symbolic links
        - `/dev/sg*` - generic SCSI device driver interface
        - `/dev/sd*` - for SCSI and SATA
        - `/dev/hd*` - for IDE
        - `/dev/md*` - for RAID arrays
        - `/dev/nvme*n*` - for NVME drives
        - `/dev/loop*` - helper for files to access block devices (Also known as vnode disk (vnd), and loopback file interface (lofi)) (`losetup` is for set up and control of loop devices)
        - `/dev/mapper/*` - Entries in that directory are [LVM](https://en.wikipedia.org/wiki/Logical_Volume_Manager_(Linux)) logical volumes. They are like Linux native partition type. Linux also supports other partitions such as PC (MBR or GPT)
    - Each invidual partitions found by the Kernel are numbered (e.g.: sda1, sda2, hda1)
- Partition block devices == contiguous sequence of disk sectors
- `mknod` is the command for creation of devices files
    - It is done automatically
    - Past system: `devfs`
    - `udev` is the program that loads devices (the deamon can be `systemd-udevd`)
    - The Kernel is the one calling `udev`
    - The event information can also be found in the `dbus`

> IMPORTANT! Forensic tools should examine raw devices and partitions without the mounting of a filesystem.

> Operations for imaging are done at the block device below the system and partition scheme.

> When doing forensic acquisition and analysis activities, understanding Linux device tree is important
> 
> Important to find: 
> - suspect drive
> - write blocker
> - [...]

#### In `/dev` (storage)
- In `/dev` directory attached drives will appear as *block devices*
- A contiguous sequence of disk sectors are partition block devices
- A partition contains: 
    - filsesystem (that can be mounted by the kernel)

## Filesystems
- List of supported filesystems: https://en.wikipedia.org/wiki/Category:File_systems_supported_by_the_Linux_kernel
- VFS (Virtual File System) is a abstraction layer to provide a consistent interface for different file system types
- The VFS allows the mounting of: 
    - EXT&#42;
    - NTFS
    - FAT
    - network-based filesystems: 
        - nfs
        - sambafs/smbfs
    - userspace filesystems based on [FUSE](https://en.wikipedia.org/wiki/Filesystem_in_Userspace)
    - stackable filesystems
        - encryptfs
        - unionfs
    - other pseudo filesystems: 
        - sysfs
        - proc
    - many others 

> NOTE: When performing forensic acquisition file system support is not necessary.Imaging process is done at the block device level (it is under the file system and the partition scheme)

This diagram helps you understand the relationship among (within the Linux kernel):
- filesystems
- devices
- device drivers
- hardware devices

![](./assets/Linux-storage-stack-diagram_v4.10.png)
*The Linux Storage Stack Diagram (Source: https://www.thomas-krenn.com/en/wiki/Linux_Storage_Stack_Diagram, used under CC Attribution-ShareAlike 3.0 Unported)*

### Mounting vs Attached disk
- To acquire a device or even access it with forensic analysis tools **it does not need to be mounted**.
- Mounting means that the standard file access tools like fila managers and other applications can access it.
- Once it is mounted it will be apart of Linux filesystem tree.
- Called *mount point* (e.g.: `/mnt` attached to it you have your drive) (`mount /dev/sdb1 /mnt`)
- To unmount: `umount /mnt` or `umount /dev/sdb1` (those are just examples your storage device might be name differently)
- You need to `umount` to prevent filesystem corruption
- After an `umount` the raw disk is still visible to the kernel and accessible bye block device tools

> **IMPORTANT!** Don't attach or `mount` a drive (you are investigating) without a write block. It might modify, damage, and destroy evidence.
> In modern OS for example it could change the timestamps as the files and directories are accessed.
> Userspace deamons can also cause changes (e.g.: search indexers, thumbnail generators, etc).
> The journaling FS could be overwriten.

> **NOTE:** A *write blocker* will make the drive that is mounted read-only.

> **NOTE:** with forensic tools you can access filesystems without `mount`.
> If the tools cannot identify the FS you might need to specify it.

The reasons why a FS might not be identify by the kernel: 
- FS is not supported by the host (lacking the kernel module or they are just no existing support)
- Partition table is corrupted or missing
- Deleted partition
- FS offset on the disk is unknown
- FS needs to be made accessible (unlock device, decrypt partition, etc)

### Forensic image formats
 


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
- You can also get information about a devices associated files/paths: `udevadm info /dev/<device>`

## `udevadm`
- For monitoring devices being removed and added: `udevadm monitor`
- Get the list of the associated files and paths for attached devices: `udevadm info /dev/sdf`

## Resources
- [`/dev`](https://tldp.org/LDP/abs/html/devref1.html)
- [Managing devices in Linux | Opensource.com](https://opensource.com/article/16/11/managing-devices-linux)
### Videos
- [Kali Linux - vid 19 - Howto use forensic image acquisition and burning tool (dc3dd) - Linux Academy | YouTube](https://www.youtube.com/watch?v=u9KNWItM3o0)
