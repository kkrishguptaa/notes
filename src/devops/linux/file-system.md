# 📂 File System

The linux file system is mostly the same between different distributions. Certain directories are for certain things. Let's look at it in detail.

## Categories

With two metrics, we can categorize the directories:

1. Whether the data is changing often or not
2. Whether the data is shared between different hosts or not

## Filesystem Hierarchy Standard

FHS is a stamdard that tells which directory should contain what. It is followed by most linux distributions.

* [FHS Spec 3.0](https://refspecs.linuxfoundation.org/FHS\_3.0/fhs-3.0.pdf)

## Directories

| Directory     | Description                                                                                                           |
| ------------- | --------------------------------------------------------------------------------------------------------------------- |
| /             | Primary directory of the entire filesystem hierarchy                                                                  |
| /bin          | Essential executable programs that must be available in single user mode                                              |
| /boot         | Files needed to boot the system, such as the kernel, initrd or initramfs images, and boot configuration files and     |
| /dev          | Device Nodes, used to interact with hardware and software devices                                                     |
| /etc          | System-wide configuration files                                                                                       |
| /home         | User home directories, including personal settings, files, etc.                                                       |
| /lib          | Libraries required by executable binaries in /bin and /sbin                                                           |
| /lib64        | 64-bit libraries required by executable binaries in /bin and /sbin, for systems which can run both 32-bit and         |
| /media        | Mount points for removable media such as CDs, DVDs, USB sticks, etc.                                                  |
| /mnt          | Temporarily mounted filesystems                                                                                       |
| /opt          | Optional application software packages                                                                                |
| /proc         | Virtual pseudo-filesystem giving information about the system and processes running on it. Can be used to alter       |
| /run          | Run-time variable data, containing information describing the system since it was booted. Replaces the older /var/run |
| /sys          | Virtual pseudo-filesystem giving information about the system and processes running on it. Can be used to alter       |
| /root         | Home directory for the root user                                                                                      |
| /sbin         | Essential system binaries                                                                                             |
| /srv          | Site-specific data served up by the system. Seldom used.                                                              |
| /tmp          | Temporary files; on many distributions lost across a reboot and may be a ramdisk in memory.                           |
| /usr          | Multi-user applications, utilities and data; theoretically read-only.                                                 |
| /var          | Variable data that changes during system operation                                                                    |
| /misc[^1]     | Used for misc. files                                                                                                  |
| /tftpboot[^2] | Used for booting tftp                                                                                                 |

### /bin & /sbin

Contains executables and scripts.

Required files: cat, chgrp, chmod, chown, cp, date, dd, df, dmesg, echo, false, hostname, kill, ln, login, ls, mkdir, mknod, more, mount, mv, ps, pwd, rm, rmdir, sed, sh, stty, su, sync, true, umount and uname

Optional files: test, csh, ed, tar, cpio, gunzip, zcat, netstat and ping

{% hint style="info" %}
Recent versions of Linux distributions have abandoned /usr/bin and /bin distinction. They are now merged into /usr/bin. Same goes for /usr/sbin and /sbin.
{% endhint %}

Required for /sbin: fdisk, fsck, getty, halt, ifconfig, init, mkfs, mkswap, reboot, route, swapon, swapoff, update.

### /boot

Required files: vmlinuz (compressed linux kernel), initramfs (initial RAM filesystem)

Optional files: config (configure kernal compilation), System.map (debugging symbols for the kernel)

{% hint style="info" %}
Instead of initramfs, some distributions use initrd (initial RAM disk). They are similar.
{% endhint %}

### /dev

It has device nodes.

### /etc

System-wide configuration files.

Required files: csh.login, exports, fstab, ftpusers, gateways, gettydefs, group, host.conf, hosts.allow, hosts.deny, hosts.equiv, hosts.lpd, inetd.conf, inittab, issue, ld.so.conf, motd, mtab, mtools.conf, networks, passwd, printcap, profile, protocols, resolv.conf, rpc, securetty, services, shells, syslog.conf.

{% hint style="info" %}
Some of these files are obsolete and not used anymore. (eg. mtools.conf)
{% endhint %}

{% hint style="info" %}
Red Hat based distributions have /etc/sysconfig directory. It contains configuration files for various services.
{% endhint %}

#### Important Subdirectories

It has skeleton/template files for new home directories

Scripts for starting and stopping services

Startup and shutdown scripts

### /home & /root

/home/username is the home directory for the user username.

This directory is added to `$HOME` environment variable and is available as `~` in the shell.

\{% hint style="info" } For root user, the home directory is `/root`.

### /lib & /lib64

Libraries required by executables in /bin and /sbin.

### /media

Mount points for removable media such as CDs, DVDs, USB sticks, etc.

### /mnt

Mount points for temporarily mounted filesystems.

### /opt

For software that would like to be isolated from the rest of the system. It is not used much.

### /proc (Process Information Pseudo-filesystem)

Virtual filesystem that provides information about the system and processes running on it.

### /sys (System Information Pseudo-filesystem)

Virtual filesystem that provides information about the system and processes running on it. Similar to a device tree and is part of the Unified Device Model.

### /srv (Service Data)

Site-specific data served up by the system.

### /tmp (Temporary Files)

Temporary files; on many distributions lost across a reboot and may be a ramdisk in memory.

### /usr (Unix System Resources)

Multi-user applications, utilities and data; theoretically read-only.

### /var (Variable Data)

Variable data that changes during system operation.

### /run (Run-time Variable Data)

Stores transient files that are not needed across reboots. It is a replacement for /var/run and /var/lock.

[^1]: Optional, Used for misc. files

[^2]: Optional, Used for booting tftp
