# Awesome WSL 
[![Awesome][awesomelogo]](https://awesome.re)

A collection of Windows Subsystem for Linux information, distributions, and tools.

## Table of Contents
* [FAQ](#faq)
* [Supported Distributions](#supported-distributions)
* [Unofficial Distributions](#unofficial-distributions)
* [WSL Tools](#wsl-tools)
* [Additional Resources](#additional-resources)

## FAQ

### What is Linux?

Linux is a [UNIX-like](https://github.com/sirredbeard/Awesome-UNIX#frequently-asked-questions) [open-source](https://opensource.org/osd) operating system. The core of Linux is a kernel (the piece of the operating system that lies between the hardware and the applications you choose to run) developed by Linus Torvalds. Linux also includes a wide array of applications, including web servers, compilers, and e-mail clients, developed and contributed by tens of thousands of programmers. These applications are then bundled together into distributions by communities, companies, and individuals.

### What is a Linux distribution?

Unlike Windows there are many different Linux distributions, each of which is assembled with different approaches to software selection and implementation. For example, the goal of the non-profit volunteer Debian Project community is to produce a universal operating system. There are also Linux distributions based on other distributions. Ubuntu is a distribution based on Debian built by for-profit company Canonical for paid use in the enterprise market. Kali is a distribution based on Debian built with an emphasis on tools for network security testing.

### What is Windows?

Windows is a family of proprietary operating systems, all of which are developed, marketed, and sold by Microsoft. Windows Subsystem for Linux first shipped in Windows 10 Anniversary Update, version number 1607, in August 2016. WSL can be enabled on all versions of Windows after 1607, including Home, Professional, Enterprise, Server, LTSB, and Education.

### What is the Windows Subsystem for Linux?

Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10. WSL provides a Linux-compatible kernel interface developed by Microsoft, which can then run a Linux userland of the users choice on top of it. It is the successor to defunct [Windows Services for UNIX](https://en.wikipedia.org/wiki/Windows_Services_for_UNIX).

### Is Windows Subsystem for Linux an emulator?

No. Windows Subsystem for Linux is not an emulator, or like Wine, or VirtualBox. WSL executes unmodified Linux ELF64 binaries by emulating a Linux kernel interface on top of the Windows NT kernel.

### How does Windows Subsystem for Linux work?

* [Windows Subsystem for Linux Overview](https://blogs.msdn.microsoft.com/wsl/2016/04/22/windows-subsystem-for-linux-overview/) at MSDN. 
* [WSL File System Support](https://blogs.msdn.microsoft.com/wsl/2016/06/15/wsl-file-system-support/) at MSDN.
* [WSL System Calls](https://blogs.msdn.microsoft.com/wsl/2016/06/08/wsl-system-calls/) at MSDN.
* [Windows and Ubuntu Interoperability](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/) at MSDN.
* [WSL Antivirus and Firewall Compatibility](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/) at MSDN.
* [WSL Release Notes](https://docs.microsoft.com/en-us/windows/wsl/release-notes) from docs.microsoft.com.
* [Windows Subsystem for Linux Documentation](https://docs.microsoft.com/en-us/windows/wsl/about) from docs.microsoft.com.
* [Windows Subsystem for Linux - Update](https://www.youtube.com/watch?v=PP_T_m0UV9E) from Microsoft Developer YouTube channel. 

### How do I install the Windows Subsystem for Linux?

* [Windows 10 Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10) - Microsoft's official documentation.
* [Windows-Subsystem-For-Linux-Setup](https://github.com/michaeltreat/Windows-Subsystem-For-Linux-Setup) - A basic guide for how to get setup with the WSL feature that is included with Windows 10. ![github project][githublogo]

### What can I do with Windows Subsystem for Linux?

WSL is undoubtedly a tool for power users, developers, and *NIX/Linux geeks who want to run Windows. Most of the things you can do with WSL are going to be related to programming, sysadmin, automation, AI/data science, and other geeky things.

#### WSL Command Line

* [Everything You Can Do With Windows 10’s New Bash Shell](https://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/)
* [The Unix Workbench](http://seankross.com/the-unix-workbench/) - A book for anyone to get started with Unix/Linux.
* [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line) - Master the command line in one page. ![github project][githublogo]
* [The Bash Academy](http://www.bash.academy) - The Bash Academy is an initiative to promote the bash shell language and educate people on its use.
* [Awesome Command Line Apps](https://github.com/herrbischoff/awesome-command-line-apps) [![Awesome][awesomelogo]](https://awesome.re) ![github project][githublogo]

#### WSL Programming

* [Epic Development Environment using Windows Subsystem for Linux](https://medium.com/@johnwoodruff91/epic-dev-environment-with-wsl-dc81e234ae61)
* [Setting Up a Programming Environment via Windows 10 Bash](https://www.cs.odu.edu/~zeil/FAQs/Public/win10Bash/)
* [Using WSL and MobaXterm to Create a Linux Dev Environment on Windows](https://nickjanetakis.com/blog/using-wsl-and-mobaxterm-to-create-a-linux-dev-environment-on-windows)
* [ubuntu-win-boostrap](https://github.com/seapagan/ubuntu-win-bootstrap) - A very simple bootstrap script to install some development tools on Debian/Ubuntu on WSL. ![github project][githublogo]
* [Castle-Winbuntu](https://github.com/rodtreweek/Castle-Winbuntu) - Another developer's setup using WSL. ![github project][githublogo]


#### WSL Web Development

* [We put Linux in your Windows with Sarah Cooley](https://www.youtube.com/watch?v=JZCPYWrTLTg) - YouTube talk by Windows kernel team member on WSL for Windows.
* [Setting Up Windows for Web Development](https://blog.cloudboost.io/setting-up-windows-for-web-development-28483d245a82)

### Can I install Linux GUI apps?

Yes, some of them. This first requires installation of X server application such as [VcXsrv](https://sourceforge.net/projects/vcxsrv/) (recommended) or [Xming](https://sourceforge.net/projects/xming/) on Windows 10.

Then in WSL type the following:

```bash
echo "export DISPLAY=:0" >> .bashrc
echo "export LIBGL_ALWAYS_INDIRECT=1" >> .bashrc
```

and restart WSL. The above commands point WSL to the X server you installed on Windows and offloads hardware graphics acceleration to Windows for faster graphical rendering.

# Supported Distributions

### Ubuntu

Ubuntu is a Linux distribution based on Debian that is produced by [Canonical](https://www.ubuntu.com/). Ubuntu 16.04 and the more recent Ubuntu 18.04 featureing more recent software are both available for WSL.

* [Windows Store Link](https://www.microsoft.com/store/productId/9NBLGGH4MSV6) for Ubuntu 16.04.
* [Windows Store Link](https://www.microsoft.com/store/productId/9N9TNGVNDL3Q) for Ubuntu 18.04.
* [Installing Software](https://help.ubuntu.com/community/InstallingSoftware) guide from Ubuntu.
* [Ubuntu Server Guide](https://help.ubuntu.com/lts/serverguide/index.html) from Ubuntu.
* Because Ubuntu is based on Debian, most Debian tutorials also apply to Ubuntu.

### Debian

Debian is a Linux distribution assembled by the non-profit [Debian](https://www.debian.org/) Project.

* [Windows Store Link](https://www.microsoft.com/store/productId/9MSVKQC78PK6).
* [Debian Reference](https://www.debian.org/doc/manuals/debian-reference/) post-installation guide for Debian users with a focus on the command line from Debian.
* [Package Management](https://www.debian.org/doc/manuals/debian-reference/ch02.en.html) from Debian.

### OpenSUSE

OpenSUSE is a Linux distribution produced by [SUSE Linux GmbH](https://www.opensuse.org/) and other companies. Leap 42 is a community-oriented distribution with recent software. SUSE Enterprise Linux is an enterprise-grade commercial distribution with older tested software.

* [Windows Store Link](https://www.microsoft.com/store/productId/9NJVJTS82TJX) for Leap 42.
* [Windows Store Link](https://www.microsoft.com/store/productId/9P32MWBH6CNS) for SUSE Enterprise Linux.
* [Managing Software with Command Line Tools](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/cha.sw_cl.html) from OpenSUSE.
* [OpenSUSE 42 Reference](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/book.opensuse.reference.html).
* [SUSE Linux Enterprise Documentation](https://www.suse.com/documentation/sles-12/index.html) from SUSE.

### Kali Linux

Kali Linux is a Linux distribution focused on penetration testing based on Debian that is produced by [Offensive Security](https://www.kali.org/).

* [Windows Store Link](https://www.microsoft.com/store/productId/9PKR34TNCV07).
* [Kali Linux Official Documentation](https://www.kali.org/kali-linux-documentation/).
* Because Kali is based on Debian, most Debian tutorials also apply to Kali.

# Unofficial Distributions

Unofficial distributions must be installed manually or with tools listed below. They are not available in the Windows Store.

* [miniwsl](https://github.com/0xbadfca11/miniwsl) - A mini Linux distribution for WSL powered by [busybox](https://www.busybox.net/). ![github project][githublogo]
* [ArchWSL](https://github.com/yuk7/ArchWSL) - ArchLinux in WSL. ![github project][githublogo]
* [AlpineWSL](https://github.com/yuk7/AlpineWSL) - Alpine in WSL. ![github project][githublogo]
* [WSLInstall](https://github.com/Biswa96/WSLInstall) - Install any GNU/Linux distribution userspace in Windows Subsystem for Linux (WSL) with compressed RootFS tarballs, Docker containers, or ISO files. ![github project][githublogo]
* [WSL-Distribution-Switcher](https://github.com/RoliSoft/WSL-Distribution-Switcher) - Scripts to replace the distribution behind WSL with any other Linux distribution published on [Docker Hub](https://hub.docker.com/explore/). Includes alpine, CentOS, Fedora, Clear, and others. ![github project][githublogo]

# WSL Tools

### Terminals

* [wsltty](https://github.com/mintty/wsltty) - Mintty as a terminal for WSL. ![github project][githublogo]
* [wsl-terminal](https://github.com/goreliu/wsl-terminal) - A terminal emulator for WSL, based on mintty, fatty and wslbridge. ![github project][githublogo]
* [ConEmu](https://conemu.github.io) - ConEmu aims to be handy, comprehensive, fast and reliable terminal where you may host any console application for the Windows command line, PowerShell, or WSL. 
* [MobaXterm](https://mobaxterm.mobatek.net/) - Enhanced terminal for Windows with X11 server, tabbed SSH client, network tools and much more.
* [extraterm](https://github.com/sedwards2009/extraterm) - Open source project to build a terminal emulator and expand it with new features to support modern workflows. ![github project][githublogo]

### Other

* [LxRunOffline](https://github.com/DDoSolitary/LxRunOffline) - A full-featured utility for managing WSL. ![github project][githublogo]
* [wslu](https://github.com/patrick330602/wslu) - A collection of utilities for Windows 10 Linux Subsystem, such as enabling sound in WSL and creating your favorite linux GUI application shortcuts on Windows 10. ![github project][githublogo]
* [BootShellCredentialProvider](https://github.com/NathanCastle/BootShellCredentialProvider) - BSCP lets you boot Windows directly into a Linux desktop experience such as xfce4 using Windows native login and a combination of Xming & WSL upon login. ![github project][githublogo]
* [wsl-dotfiles](https://github.com/Xyene/wsl-dotfiles) - Configuration files and scripts for creating an i3-based environment inside WSL. ![github project][githublogo]
* [wslgit](https://github.com/andy-5/wslgit) - Use git installed WSL from Windows and Visual Studio Code (VSCode). ![github project][githublogo]
* [wsl-proxy](https://github.com/watzon/wsl-proxy) - A collection of "proxy" batch files that can be used to route requests to the WSL version of a command. ![github project][githublogo]
* [wslpath](https://github.com/laurent22/wslpath) - PHP app to convert Windows and WSL path names. ![github project][githublogo]
* [wsl-open](https://github.com/4U6U57/wsl-open) - Open files with xdg-open on Bash for Windows in Windows applications. ![github project][githublogo]
* [wsl-docker-git-setup](https://github.com/rodtreweek/Castle-Winbuntu) - Shell script to configure WSL to use docker and docker-compose as well as a git-enabled prompt. ![github project][githublogo]
* [VcXsrv](https://sourceforge.net/projects/vcxsrv/) - X server for Windows. Required for running Linux GUI apps in Windows.

# Additional Resources

* [The Windows Subsystem for Linux Guide](http://wsl-guide.org/en/latest/) - Third-party WSL resource.
* [WSL-Programs](https://github.com/ethanhs/WSL-Programs) - A community powered list of programs that work on the Windows Subsystem for Linux. ![github project][githublogo]
* [/r/bashonubuntuonwindows](https://www.reddit.com/r/bashonubuntuonwindows/)
* [WSL-DistroLauncher](https://github.com/Microsoft/WSL-DistroLauncher) - Reference launcher app for developing your own WSL distribution Microsoft Store packages. ![github project][githublogo]
* [Ansible-WSL](https://github.com/Wintus/Ansible-WSL) - Provision WSL using Ansible.

# More

* [Awesome Windows](https://github.com/Awesome-Windows/Awesome)
* [Awesome VSCode](https://github.com/viatsko/awesome-vscode)
* [Awesome Bash](https://github.com/awesome-lists/awesome-bash)
* [Awesome Shell](https://github.com/alebcay/awesome-shell)
* [Awesome Powershell](https://github.com/janikvonrotz/awesome-powershell)

More [![Awesome][awesomelogo]](https://awesome.re) lists. ![github project][githublogo]

------

* Linux® is a registered trademark of Linus Torvalds in the United States and/or other countries.
* Windows®, Microsoft®, Skype®, Windows NT®, and Xenix® are trademarks or registered trademarks of Microsoft Corporation in the United States and/or other countries.
* Ubuntu® and Canonical® are registered trademark of Canonical Limited in the United States and/or other countries.
* SUSE® and SUSE Linux Enterprise® are registered trademarks of SUSE in the United States and/or other countries.

All other trademarks mentioned herein are the property of their respective owners and may be registered in the United States and/or other countries.

Portions of the descriptions above are from Wikipedia and used under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/). Portions of the descriptions above are from [Awesome-UNIX](https://github.com/sirredbeard/Awesome-UNIX) and used under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/).

This document is licensed under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/).

[githublogo]:https://raw.githubusercontent.com/sirredbeard/Awesome-WSL/master/github-icon.png
[awesomelogo]:https://awesome.re/badge.svg
