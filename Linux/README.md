# Linux | Forensic Imaging | Quickstarts
There are many open-source tools out there to help with forensic imaging.

This section is all about the Linux tools.

## Command list
- `sg_raw`
- `dmesg`
- `blockdev`

## Setup
### Debian
- `sg3-utils` this includes tools like `sg_raw` (SCSI or NVMe disks)
```bash
sudo apt update
sudo apt install -y sg3-utils
```
