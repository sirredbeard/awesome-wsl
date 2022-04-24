# Awesome WSL - Windows Subsystem for Linux
[![Awesome][awesomelogo]](https://awesome.re)

An Awesome collection of Windows Subsystem for Linux (WSL) information, distributions, and tools.

![WSLscreenshot](https://user-images.githubusercontent.com/33820650/145261380-a0dd2834-4830-4272-8a5b-4547fb40c296.PNG)


## Contents
- [Overview](#overview)
- [Using WSL](#using-wsl) </br>
          - [The WSL Shell](https://github.com/sirredbeard/Awesome-WSL#the-wsl-shell) <br>
          - [Programming on WSL](https://github.com/sirredbeard/Awesome-WSL#programming-on-wsl) <br>
          - [Web Development on WSL](https://github.com/sirredbeard/Awesome-WSL#web-development-on-wsl) <br>
          - [Other WSL Uses](https://github.com/sirredbeard/Awesome-WSL#other-wsl-uses)
- [Supported WSL Distributions](#supported-distributions) </br>
          - [Ubuntu](https://github.com/sirredbeard/Awesome-WSL#ubuntu) <br>
          - [Debian](https://github.com/sirredbeard/Awesome-WSL#debian) <br>
          - [OpenSUSE / SUSE Enterprise Linux](https://github.com/sirredbeard/Awesome-WSL#opensuse--suse-enterprise-linux) <br>
          - [Kali Linux](https://github.com/sirredbeard/Awesome-WSL#kali-linux) <br>
          - [Fedora Remix for WSL](https://github.com/sirredbeard/Awesome-WSL#fedora-remix-for-wsl) <br>
          - [Pengwin](https://github.com/sirredbeard/Awesome-WSL#pengwin) <br>
          - [Pengwin Enterprise](https://github.com/sirredbeard/Awesome-WSL#pengwin-enterprise) <br>
- [Unofficial WSL Distributions](#unofficial-distributions)
- [WSL Tools](#wsl-tools) <br>
          - [X Servers](https://github.com/sirredbeard/Awesome-WSL#x-servers) <br>
          - [Terminals](https://github.com/sirredbeard/Awesome-WSL#terminals) <br>
          - [Managing WSL Installations](https://github.com/sirredbeard/Awesome-WSL#for-managing-wsl) <br>
          - [WSL Utilities](https://github.com/sirredbeard/Awesome-WSL#wsl-utilities) <br>
          - [WSL-Specific Development Tools](https://github.com/sirredbeard/Awesome-WSL#wsl-specific-development-tools) <br>
          - [Miscellaneous Tools](https://github.com/sirredbeard/Awesome-WSL#miscellaneous-tools)
- [Books](#books)
- [Additional WSL Resources](#additional-resources)
- [Related Projects](#related-projects)
- [More Awesome Lists](#more-awesome)
- [Thanks](#thanks)
- [Intellectual Property Notices](#intellectual-property-notices)

## Overview

### 1. Linux

Linux is a [UNIX-like](https://github.com/sirredbeard/Awesome-UNIX#frequently-asked-questions) [open-source](https://opensource.org/osd) operating system. The core of Linux is a [kernel](https://www.howtogeek.com/howto/31632/what-is-the-linux-kernel-and-what-does-it-do) developed by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds). Linux also includes a wide array of applications built on top of the kernel, including [web servers](https://www.linux.com/learn/apache-ubuntu-linux-beginners), [compilers](https://gcc.gnu.org), and [e-mail clients](https://wiki.gnome.org/Apps/Geary), developed and contributed to the Linux ecosystem by a worldwide community of programmers. These applications are then assembled together into Linux [distributions](https://en.wikipedia.org/wiki/Linux_distribution) by [companies](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), [communities](https://www.archlinux.org), and [individuals](http://www.slackware.com).

### 2. Linux Distributions

Unlike Windows or macOS there are many different Linux distributions, each of which is assembled with different approaches to the software selection and implementation. For example, the goal of the non-profit volunteer [Debian Project](https://www.debian.org/devel/constitution) community is to produce a universal free operating system, while the goal of the for-profit SUSE is to provide a [stable enterprise platform](https://www.suse.com). There are also Linux distributions based on other distributions. [Ubuntu](https://www.ubuntu.com) is a distribution based on Debian built by the company Canonical. Kali is a distribution based on Debian built with an emphasis on tools for network security testing. You can see the most popular distributions ranked at [DistroWatch](https://distrowatch.com).

### 3. Windows

[Windows](https://en.wikipedia.org/wiki/Microsoft_Windows) is a family of proprietary operating systems, all of which are developed, marketed, and sold by Microsoft. Currently Windows 10 is Microsoft's flagship operating system. Windows 10 is available for Intel x86-based and arm64-based PCs. The Windows Subsystem for Linux first shipped in [Windows 10 Anniversary Update](https://blogs.msdn.microsoft.com/wsl/2016/07/08/bash-on-ubuntu-on-windows-10-anniversary-update/), version number 1607, in August 2016. WSL can be enabled for free on all versions of Windows 10 after 1607, including Home, Professional, Enterprise, Server, LTSB, and Education. Originally only available for Intel x86-based PCs, Ubuntu 18.04 for arm64 was made available on the Microsoft store in [May 2018](https://twitter.com/TheRealHariP/status/994293523514970112).

### 4. WSL1

The original WSL is now known as WSL1. WSL1 is a compatibility layer for running Linux binary executables (ELF) natively on Windows 10. No re-compilation or 'porting' of applications is required. WSL1 provides a Linux-compatible kernel interface developed by Microsoft that allows a user to choose a Linux distribution to install from the Microsoft Store. WSL1 executes unmodified Linux ELF64 binaries by operating a Linux kernel interface on top of the Windows kernel in Windows 10. The WSL1 interface translates Linux system calls from the binaries into Windows system calls and then executes them at native speed. Linux applications run within the Linux distribution which provides the application's dependencies and package management in a container-like environment. WSL provides an interface to mount drives within WSL.

### 5. WSL2

WSL2 was announced at Microsoft Build 2019. WSL2 features a Linux kernel running inside Windows and is built on the core technology of Hyper-V to provide better Linux application support and improved file system performance. Transitioning to WSL2 is seamless. WSL2 is set by default since Windows 11.

- [Announcing WSL2](https://devblogs.microsoft.com/commandline/announcing-wsl-2/) - Microsoft blog announcing WSL2
- [The new Windows subsystem for Linux architecture: a deep dive](https://www.youtube.com/watch?v=lwhMThePdIo) - WSL2 presentation at Microsoft Build 2019
- [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) - The source for the Linux kernel used in Windows Subsystem for Linux 2. 

### 6. Emulation

Windows Subsystem for Linux is not an emulator or virtualizer like [VirtualBox](https://www.virtualbox.org). WSL1 is closer in its approach to [Wine](https://www.winehq.org) which is a compatibility layer to run Windows binaries on Linux by re-implementing Windows system and API calls in libraries.

### 7. Details

You want the gritty details? Here they are:

- [Windows Subsystem for Linux Overview](https://blogs.msdn.microsoft.com/wsl/2016/04/22/windows-subsystem-for-linux-overview/) at MSDN. 
- [WSL File System Support](https://blogs.msdn.microsoft.com/wsl/2016/06/15/wsl-file-system-support/) at MSDN.
- [WSL System Calls](https://blogs.msdn.microsoft.com/wsl/2016/06/08/wsl-system-calls/) at MSDN.
- [Windows and Ubuntu Interoperability](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/) at MSDN.
- [WSL Antivirus and Firewall Compatibility](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/) at MSDN.
- [WSL Release Notes](https://docs.microsoft.com/en-us/windows/wsl/release-notes) from docs.microsoft.com.
- [Windows Subsystem for Linux Documentation](https://docs.microsoft.com/en-us/windows/wsl/about) from docs.microsoft.com.
- [Windows Subsystem for Linux - Update](https://www.youtube.com/watch?v=PP_T_m0UV9E) from Microsoft Developer YouTube channel. 
- [Windows for Linux Nerds](https://blog.jessfraz.com/post/windows-for-linux-nerds/) from Microsoft developer Jessie Frazelle.

### 8. Installation

- [WSL1 Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install) - Microsoft's official guide for WSL.
- [Windows Server Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-on-server) - Microsoft's official guide for Windows Server.
- [Windows-Subsystem-For-Linux-Setup](https://github.com/michaeltreat/Windows-Subsystem-For-Linux-Setup) - A basic guide for how to get setup with the WSL feature that is included with Windows 10. ![github project][githublogo]

### 9. Use Cases

WSL is undoubtedly a tool for power-users, developers, and *NIX/Linux geeks who want to run Windows. Most of the things you can do with WSL are going to be related to programming, the console, sysadmin, automation, AI/data science, and other geeky things.

### 10. GUI Apps

Yes, a [suprising number](https://github.com/ethanhs/WSL-Programs) of Linux GUI apps can run on WSL. GUI applications are officially supported on WSL2 with Windows Insider Preview since Windows 10 Insider Preview build 21286. It will also be available in Windows 10's fall 2021 release, and Windows 11. The GUI capabilities of WSL2 are informally referred to as WSLg.

If you have an earlier release of Windows 10, then running a GUI app on WSL requires an operational X server on Windows. This must be downloaded, installed, and running for your GUI app to open from WSL; or it will complain that it cannot find a display. X servers for Windows include [X410](https://afflnk.microsoft.com/c/1291904/433017/7593?u=https%3A%2F%2Fwww.microsoft.com%2Fp%2Fx410%2F9nlp712zmn9q) 💰 ($10 but very highly recommended), [VcXsrv](https://sourceforge.net/projects/vcxsrv/), [GWSL](https://www.microsoft.com/store/apps/9NL6KD1H33V3), or [Xming](https://sourceforge.net/projects/xming/) on Windows 10.

## Using WSL

#### The WSL Shell

- [Everything You Can Do With Windows 10’s New Bash Shell](https://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/)
- [The Unix Workbench](http://seankross.com/the-unix-workbench/) - A book for anyone to get started with Unix/Linux environments.
- [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line) - Master the command line in one page. ![github project][githublogo]
- [The Bash Academy](http://www.bash.academy) - The Bash Academy is an initiative to promote the bash shell language and educate people on its use.
- [Awesome Command Line Apps](https://github.com/herrbischoff/awesome-command-line-apps) [![Awesome][awesomelogo]](https://awesome.re) ![github project][githublogo]

#### Programming on WSL

Every developer has a unique workflow. Windows and WSL enable developers to carefully customize their setup for their unique workflow. The following are different developers' approaches to creating their development environments using WSL and instructions on how to do the same:

- [Epic Development Environment Using Windows Subsystem for Linux](https://medium.com/@johnwoodruff91/epic-dev-environment-with-wsl-dc81e234ae61) - One developer's approach to their development environment using WSL1.
- [Far More Epic Development Environment using WSL2](https://dev.to/johnbwoodruff/far-more-epic-development-environment-using-wsl-2-439g)
- [Setting Up a Programming Environment via Windows 10 Bash](https://www.cs.odu.edu/~zeil/FAQs/Public/win10Bash/) - From the computer science department at Old Dominion University.
- [WSL as a Development Environment](https://github.com/hsab/WSL-config) - From the computer science department at University of Utah. ![github project][githublogo]
- [Using WSL and MobaXterm to Create a Linux Dev Environment on Windows](https://nickjanetakis.com/blog/using-wsl-and-mobaxterm-to-create-a-linux-dev-environment-on-windows) - Another developer's approach using the third-party terminal MobaXterm.
- [Setting up my WSL Environment - Azure CLI, Docker and .NET](http://tattoocoder.com/setting-up-my-wsl-environment-azure-cli-docker-and-net/)
- [ubuntu-win-boostrap](https://github.com/seapagan/ubuntu-win-bootstrap) - A very simple bootstrap script to install some development basic tools on Debian/Ubuntu on WSL. ![github project][githublogo]
- [Castle-Winbuntu](https://github.com/rodtreweek/Castle-Winbuntu) - Another developer's progress on their development environment using WSL. ![github project][githublogo]
- [Badass Terminal](https://jessicadeen.com/badass-terminal-wsl-macos-and-ubuntu-dotfiles-update/)

For more about learning programming generally, visit [curated-programming-resources](https://github.com/Michael0x2a/curated-programming-resources/blob/master/resources.md).

Microsoft makes [free development tools](https://code.visualstudio.com) available, publishes programming guides through [MSDN](https://msdn.microsoft.com/en-us/library/windows/desktop/ff381399(v=vs.85).aspx), and offers courses through [edX](https://www.edx.org/school/microsoft) and [Microsoft Virtual Academy](https://mva.microsoft.com).

#### Web Development on WSL

Because WSL allows developers to run a variety of Linux server applications locally on their Windows machine, WSL is uniquely useful for web, cloud, and other server-side development tasks. The following are different developers' approaches to creating their web development environment using WSL and instructions on how to do the same:

- [We put Linux in your Windows](https://www.youtube.com/watch?v=JZCPYWrTLTg) - YouTube talk by Windows kernel team member Sarah Cooley on WSL for Windows.
- [Setting Up Windows for Web Development](https://blog.cloudboost.io/setting-up-windows-for-web-development-28483d245a82).
- [How to Install LAMP Stack Server on Windows Subsystem Linux](https://medium.com/@ssharizal/how-to-install-lamp-stack-server-on-windows-subsystem-linux-wsl-windows-10-133419c22473).

#### Other WSL Uses
- [Arduino setup checklist](https://yanivpaz.com/2020-04-13-arduino-wsl1/) - Checklist to connect Arduino board from WSL 1.  
- Learning [programming](https://www.codecademy.com), [computer science](https://www.quora.com/Why-should-computer-science-students-use-the-GNU-Linux-operating-system), and [system administration](https://www.linuxfoundation.org/blog/7-steps-to-start-your-linux-sysadmin-career/) generally.
- Building applications for [Azure](https://blogs.technet.microsoft.com/stefan_stranger/2018/03/08/installing-azure-cli-on-debian-gnulinux-for-wsl/), Microsoft's cloud platform.
- Leveraging the power of the shell and scripting to automate your personal workflow, like OCRing and sorting PDFs into folders using [Python](https://www.pyimagesearch.com/2017/07/10/using-tesseract-ocr-python/).
- Replacing Windows shell [with Xfce, Gnome, KDE, or i3.](https://github.com/NathanCastle/BootShellCredentialProvider).
- Running Linux-based server applications like [OpenFOAM](https://openfoam.org/download/windows-10/) and [Wordpress](https://mkaz.blog/wordpress/install-wordpress-on-windows-subsystem-for-linux/) locally for testing purposes.
- Managing your companies' CentOS servers using [Ansible](https://www.jeffgeerling.com/blog/2017/using-ansible-through-windows-10s-subsystem-linux).
- [pWSLinux+K8S: The Interop way](https://medium.com/@hoxunn/wslinux-k8s-the-interop-way-2d98e5b88f08)
- [Vagrant and Windows Subsystem for Linux](https://www.vagrantup.com/docs/other/wsl.html)

## Supported Distributions

#### Ubuntu

Ubuntu is a Linux distribution based on Debian that is produced by [Canonical Ltd.](https://www.ubuntu.com). Ubuntu 16.04 and the more recent Ubuntu 18.04 are both available for WSL from the Microsoft Store.

- [Windows Store Link](https://www.microsoft.com/store/productId/9NBLGGH4MSV6) for Ubuntu 16.04. Supported through April 2021. Very stable but some packages and libraries may be older.
- [Windows Store Link](https://www.microsoft.com/store/productId/9N9TNGVNDL3Q) for Ubuntu 18.04. Supported through April 2023.
- [Windows Store Link](https://www.microsoft.com/en-gb/p/ubuntu-2004-lts/9n6svws3rx71?activetab=pivot:overviewtab) for Ubuntu 20.04. Most recent update. Newer packages but more likely to encounter bugs. Supported through April 2025.
- [Installing Software](https://help.ubuntu.com/community/InstallingSoftware) guide to using apt from Ubuntu.
- [Ubuntu Server Guide](https://help.ubuntu.com/lts/serverguide/index.html) from Ubuntu.
- Because Ubuntu is based on Debian, many Debian tutorials also apply to Ubuntu.

#### Debian

Debian is a Linux distribution assembled by volunteers with the community [Debian](https://www.debian.org) Project.

- [Windows Store Link](https://www.microsoft.com/store/productId/9MSVKQC78PK6) for Debian Stretch.
- [Debian Reference](https://www.debian.org/doc/manuals/debian-reference/) post-installation guide for Debian users with a focus on the command line from Debian.
- [Package Management](https://www.debian.org/doc/manuals/debian-reference/ch02.en.html) guide to using apt from Debian.
- [WSL Wiki page](https://wiki.debian.org/InstallingDebianOn/Microsoft/Windows/SubsystemForLinux) from Debian.

#### OpenSUSE / SUSE Enterprise Linux

OpenSUSE and SUSE Enterprise Linux are Linux distributions produced by [SUSE Linux GmbH](https://www.opensuse.org) and other companies. Tumbleweed and Leap are community-oriented distributions. Tumbleweed is a rolling release distribution with the latest software, while Leap is a stable distribution based on SUSE Enterprise Linux. SUSE Enterprise Linux is an enterprise-grade commercial distribution with older tested software.

- [Windows Store Link](https://www.microsoft.com/en-us/p/opensuse-tumbleweed/9mssk2zxxn11) for OpenSUSE Tumbleweed.
- [Windows Store Link](https://www.microsoft.com/en-us/p/opensuse-leap-153/9n6j06bmcgt3) for OpenSUSE Leap 15.3.
- [Windows Store Link](https://www.microsoft.com/en-us/p/opensuse-leap-152/9mzd0n9z4m4h) for OpenSUSE Leap 15.2.
- [Windows Store Link](https://www.microsoft.com/store/productId/9PMW35D7FNLX) for SUSE Enterprise Linux 15.
- [Managing Software with Command Line Tools](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/cha.sw_cl.html) from OpenSUSE.
- [OpenSUSE Reference](https://doc.opensuse.org/documentation/leap/reference/html/book.opensuse.reference/book.opensuse.reference.html).
- [SUSE Linux Enterprise Documentation](https://www.suse.com/documentation/sles-15/index.html) from SUSE.

#### Kali Linux

Kali Linux is a Linux distribution focused on penetration testing based on Debian that is produced by [Offensive Security](https://www.kali.org).

- [Windows Store Link](https://www.microsoft.com/store/productId/9PKR34TNCV07).
- [Kali Linux Official Documentation](https://www.kali.org/kali-linux-documentation/).
- Because Kali is based on Debian, most Debian and Ubuntu documentation also applies to Kali.

#### Fedora Remix for WSL

Fedora Remix for WSL is a Linux distribution derived from the [Fedora distribution](https://getfedora.org/).

- [Windows Store Link](https://www.microsoft.com/store/productId/9N6GDM4K2HNC) 💰
- [Fedora Project Documentation](https://docs.fedoraproject.org/)
- [Fedora Remix for WSL Homepage](https://www.whitewaterfoundry.com/fedora-remix-for-wsl/)
- [Fedora Remix for WSL GitHub](https://github.com/WhitewaterFoundry/WSLFedoraRemix) ![github project][githublogo]

#### Pengwin

Pengwin (formerly WLinux) is a Linux distribution based on Debian that is designed for WSL users by independent open source developers at [Whitewater Foundry](https://www.whitewaterfoundry.com/).

- [Windows Store Link](https://afflnk.microsoft.com/c/1291904/433017/7593?u=https%3A%2F%2Fwww.microsoft.com%2Fp%2Fwlinux%2F9nv1gv1pxz6p) 💰
- [Pengwin GitHub](https://github.com/WhitewaterFoundry/Pengwin) ![github project][githublogo]
- Because Pengwin is based on Debian, most Debian and Ubuntu documentation also applies to Pengwin.

#### Pengwin Enterprise

Pengwin Enterprise is a custom WSL solution available to enterprise customers from Whitewater Foundry. Pengwin Enterprise supports [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), [CentOS](https://www.centos.org/), and [Scientific Linux](https://www.scientificlinux.org/). A demo of Pengwin Enterprise built with [Scientific Linux](https://www.scientificlinux.org/) is available on the Microsoft Store.

- [Pengwin Enterprise Homepage](https://www.whitewaterfoundry.com/pengwin-enterprise)
- [Pengwin Enterprise GitHub](https://github.com/WhitewaterFoundry/Pengwin-Enterprise) ![github project][githublogo]
- Demo [Microsoft Store Link](https://www.microsoft.com/store/productId/9N8LP0X93VCP)

#### Oracle Linux

Oracle Linux is a Linux distribution based on [Red Hat Enterprise Linux](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux) that is produced by [Oracle](https://www.oracle.com/linux/).

- [Windows Store Link](https://www.microsoft.com/en-us/p/oracle-linux-79/9p7l0qwbsltk) for Oracle Linux 7 Update 9.
- [Windows Store Link](https://www.microsoft.com/en-us/p/oracle-linux-85/9p06h18wxbvp#activetab=pivot:overviewtab) for Oracle Linux 8 Update 5.
- [Oracle Linux 7 Documentation](https://docs.oracle.com/en/operating-systems/oracle-linux/7/)
- [Oracle Linux 8 Documentation](https://docs.oracle.com/en/operating-systems/oracle-linux/8/)

## Unofficial Distributions

Unofficial distributions must be installed manually or with tools listed below. They are not available in the Windows Store.

- [miniwsl](https://github.com/0xbadfca11/miniwsl) - A mini Linux distribution for WSL powered by [busybox](https://www.busybox.net). ![github project][githublogo]
- [ArchWSL](https://github.com/yuk7/ArchWSL) - ArchLinux in WSL. ![github project][githublogo]
- [AlpineWSL](https://github.com/yuk7/AlpineWSL) - Alpine in WSL. ![github project][githublogo]
- [windows-subsystem-linux-fedora](https://gitlab.com/gbraad/windows-subsystem-for-linux-fedora) - Fedora in WSL.
- [WSLInstall](https://github.com/Biswa96/WSLInstall) - Install any GNU/Linux distribution userspace in Windows Subsystem for Linux (WSL) with compressed RootFS tarballs, Docker containers, or ISO files. ![github project][githublogo]
- [wsldl](https://github.com/yuk7/wsldl) - General purpose WSL installer and launcher. ![github project][githublogo]
- [WSL-Distribution-Switcher](https://github.com/RoliSoft/WSL-Distribution-Switcher) - Scripts to replace the distribution behind WSL with any other Linux distribution published on [Docker Hub](https://hub.docker.com/explore/). Includes alpine, CentOS, Fedora, Clear, and others. ![github project][githublogo]
- [acme-wsl](https://github.com/elrzn/acme-wsl) - Install acme / plan9port on Debian, Ubuntu, or Kali Linux distributions on WSL. 
- [CentWSL](https://github.com/yuk7/CentWSL) - CentOS as a WSL distro. ![github project][githublogo]
- [RHWSL](https://github.com/yosukes-dev/RHWSL) - Red Hat Universal Base Image as a WSL distro. If you have a Red Hat Subscription, you can register and subscribe the system and use it as RHEL. ![github project][githublogo]
- [FedoraWSL](https://github.com/yosukes-dev/FedoraWSL) - Fedora as a WSL distro. ![github project][githublogo]
- [AmazonWSL](https://github.com/yosukes-dev/AmazonWSL) - Amazon Linux as a WSL distro. ![github project][githublogo]
- [GentooWSL](https://github.com/imaandrew/GentooWSL) - Gentoo as a WSL distro. ![github project][githublogo]
- [DevuanWSL](https://github.com/VPraharsha03/DevuanWSL) - Devuan Linux as a WSL Distro. Devuan is a Debian variant without the complexities and dependencies of systemd. ![github project][githublogo]
- [ManjaroWSL](https://github.com/sileshn/ManjaroWSL) - Manjaro as a WSL distro based on wsldl. ![github project][githublogo]
- [WSLackware](https://github.com/Mohsens22/WSLackware) - Slackware as a WSL distro. ![github project][githublogo]

## WSL Tools

#### X Servers

An X server running on Windows is required for running Linux GUI apps on Windows. See [FAQ #10](#10-gui-apps) above.

- [X410](https://token2shell.com/x410/) - X server for Windows 10 on the Microsoft Store. 💰
- [VcXsrv](https://sourceforge.net/projects/vcxsrv/) - X server for Windows with hardware acceleration compiled with Visual Studio.
- [GWSL](https://www.microsoft.com/store/apps/9NL6KD1H33V3) - An X server for Windows 10 with an app launcher, distro manager, shortcut creator, and ssh launcher.
- [Xmanager](https://www.netsarang.com/en/xmanager/) - X server for Windows from NetSarang. 💰
- [Xming open-source version](https://sourceforge.net/projects/xming/) - An older X server for Windows. Has not been updated since 2016.
- [Xming commercial version](http://www.straightrunning.com/XmingNotes/) - The current version of Xming, that is updated monthly. Donate at least £10 to have access to it. 💰
- [Cygwin/X](https://x.cygwin.com) - Cygwin/X is a port of the X Window System to the Cygwin API layer for Windows.

#### Terminals

- [Windows Terminal](https://github.com/microsoft/terminal) - The new open-source Windows Terminal. ![github_project][githublogo]
- [wsltty](https://github.com/mintty/wsltty) - Mintty as a terminal for WSL. ![github project][githublogo]
- [wsl-terminal](https://github.com/goreliu/wsl-terminal) - A terminal emulator for WSL, based on mintty, fatty and wslbridge. ![github project][githublogo]
- [Tabby](https://tabby.sh/) - A terminal for a more modern age. ![github project][githublogo]
- [ConEmu](https://conemu.github.io) - ConEmu aims to be handy, comprehensive, fast and reliable terminal where you may host any console application for the Windows command line, PowerShell, or WSL. 
- [MobaXterm](https://mobaxterm.mobatek.net) - Enhanced terminal for Windows with X11 server, tabbed SSH client, network tools and much more.
- [extraterm](https://github.com/sedwards2009/extraterm) - Open source project to build a terminal emulator and expand it with new features to support modern workflows. ![github project][githublogo]
- [Hyper](https://hyper.is/) - A terminal built on web technologies. ![github project][githublogo]
- [Terminator](https://medium.com/@bhupathy/install-terminator-on-windows-with-wsl-2826591d2156) - Feature-rich tabbed terminal. Requires X server.
- [Alacritty](https://github.com/alacritty/alacritty) - A terminal emulator with focus on performance and simplicity.
- [Fluent Terminal](https://github.com/felixse/FluentTerminal) - A Terminal Emulator based on UWP and web technologies.

#### For Managing WSL Installations

- [Ansible-WSL](https://github.com/Wintus/Ansible-WSL) - Provision WSL using Ansible. ![github project][githublogo]
- [LxRunOffline](https://github.com/DDoSolitary/LxRunOffline) - A full-featured utility for managing WSL. ![github project][githublogo]
- [Raft WSL](https://www.microsoft.com/store/apps/9MSMJQD017X7) - Raft is a Windows Subsystem for Linux (WSL) distribution manager in native C#/XAML. 💰
- [WSL GUI Tool](https://github.com/emeric-martineau/wsl-gui-tool) - A graphical tool to manage (run, stop, import, export...) WSL. ![github project][githublogo]
- [WSL Distro Manager](https://github.com/bostrot/wsl2-distro-manager) - GUI to manage, copy, distribute WSL distros. ![github project][githublogo]

#### WSL Utilities

- [wslgit](https://github.com/andy-5/wslgit) - Use git installed on WSL from Visual Studio Code on Windows. ![github project][githublogo]
- [pinentry-wsl-ps1](https://github.com/diablodale/pinentry-wsl-ps1) - Store passwords for gpg-agent in Windows Credential Manager ![github project][githublogo]
- [wslexec](https://github.com/int128/wslexec) - Execute Linux executables as .exe files on Windows. ![github project][githublogo]
- [wsl-proxy](https://github.com/watzon/wsl-proxy) - A collection of 'proxy' batch files that can be used to route requests to the WSL version of a command. ![github project][githublogo]
- [wslpath](https://github.com/laurent22/wslpath) - Easily convert Windows to WSL path names and vice-versa. ![github project][githublogo]
- [wsl-open](https://github.com/4U6U57/wsl-open) - Open files with xdg-open in WSL from Windows applications. ![github project][githublogo]
- [OpenInWSL](https://github.com/Opticos/OpenInWSL-Source) - Easily Make WSL Linux Apps Windows File Handlers. ![github project][githublogo]
- [is-wsl for Node](https://github.com/sindresorhus/is-wsl) - Check if the current process is running inside Windows Subsystem for Linux, useful for scripting. ![github project][githublogo]
- [is_wsl for Python](https://github.com/julien-h/is-wsl) - Check if the current process is running inside Windows Subsystem for Linux, useful for scripting. ![github project][githublogo] 
- [wsl-gui-bins](https://github.com/Konfekt/wsl-gui-bins) -  Start common GUI applications under WSL as under Linux. ![github project][githublogo]
- [xclip-xsel-WSL](https://github.com/Konfekt/xclip-xsel-WSL) -  Make `xclip` and `xsel` in `WSL` read and write on the Windows instead of the Linux clipboard.
. ![github project][githublogo]
- [vim-wsl-copy-paste](https://github.com/Konfekt/vim-wsl-copy-paste) -  Adds mappings in Vim to write and read on the Windows clipboard.
. ![github project][githublogo]
- [WslShortcut](//github.com/HanabishiRecca/WslShortcut) - Run WSL commands directly in Windows. Also allows to use WSL `git`/`node`/etc. in **Visual Studio Code** or another software. Combines functionality of utilities like [`wslgit`](//github.com/andy-5/wslgit), [`wslnodejs`](//github.com/snooopcatt/wslnodejs), [`wslexec`](//github.com/int128/wslexec) etc. with simpler usage. ![github project][githublogo]
- [community.wsl.sdk](https://github.com/Gitii/community.wsl.sdk) - SDK for Windows Subsystem for Linux for .NET 5, 6 and Standard 2.1 ![github project][githublogo]
- [wslu](https://github.com/wslutilities/wslu) - A collection of utilities for Windows 10 Linux Subsystem, such as enabling sound in WSL and creating your favorite linux GUI application shortcuts on Windows 10. ![github project][githublogo]
- [wslpy](https://github.com/wslutilities/wslpy) - A Python3 library for WSL specific tasks. ![github project][githublogo]

#### WSL-Specific Development Tools

- [wsl-docker-git-setup](https://github.com/rodtreweek/Castle-Winbuntu) - Shell script to configure WSL to use docker and docker-compose as well as a git-enabled prompt. ![github project][githublogo]
- [ghc](https://launchpad.net/~hvr/+archive/ubuntu/ghc-wsl) - A version of the Glasgow Haskell Compiler built and optimized for WSL and hosted in a PPA for Debian and Ubuntu-based WSL distros.

#### Miscellaneous Tools

- [BootShellCredentialProvider](https://github.com/NathanCastle/BootShellCredentialProvider) - BSCP lets you boot Windows directly into a Linux desktop experience such as xfce4 using Windows native login and a combination of Xming & WSL upon login. ![github project][githublogo]
- [wsl-dotfiles](https://github.com/Xyene/wsl-dotfiles) - Configuration files and scripts for creating an i3-based environment inside WSL. ![github project][githublogo]
- [EnumWSL](https://github.com/therealkenc/EnumWSL) - Enumerates installed WSL packages. ![github project][githublogo]
- [WSL-DistroLauncher](https://github.com/Microsoft/WSL-DistroLauncher) - Reference launcher app for developing your own WSL distribution Microsoft Store package. ![github project][githublogo]
- [WSL_Reverse](https://github.com/Biswa96/WSL_Reverse) - Reveal hidden COM interface between WSL and Lxss Manager Service. ![github project][githublogo]
- [wslbridge](https://github.com/rprichard/wslbridge) - wslbridge is a Cygwin program that allows connecting to the WSL command-line environment over TCP sockets, as with ssh, but without the overhead of configuring an SSH server. ![github project][githublogo]
- [WSLInstall](https://github.com/Biswa96/WSLInstall) - Install any Linux distribution userspace in WSL with compressed RootFS tarballs (tar.gz) or with Docker containers or with ISO files. ![github project][githublogo]
- [cmd-colors-solarized](https://github.com/neilpa/cmd-colors-solarized) - This is a solarized color scheme for the Windows command prompt that works in WSL.
- [weasel-pageant](https://github.com/vuori/weasel-pageant) - An ssh-agent compatible helper for interacting with Pageant from processes running on the Windows Subsystem for Linux.
- [wsl2-ssh-pageant](https://github.com/BlackReloaded/wsl2-ssh-pageant) - A bridge between Windows Pageant and WSL2.
- [WinCryptSSHAgent](https://github.com/buptczq/WinCryptSSHAgent) - Using a Yubikey for SSH Authentication on Windows Seamlessly.  Supports WSL and WSL2.
- [Files](https://github.com/files-community/Files) - A modern file explorer that supports WSL filesystem. ![github project][githublogo]
- [easyWSL](https://github.com/redcode-labs/easyWSL) - Use any Docker image as a WSL distro. ![github project][githublogo]
- [setup-wsl](https://github.com/Vampire/setup-wsl) - A GitHub action to install and setup a Linux distribution for the Windows Subsystem for Linux (WSL). ![github project][githublogo]

## Books

- [Learn Windows Subsystem for Linux](https://www.apress.com/gp/book/9781484260371) - A Practical Guide for Developers and IT Professionals
- [Pro Windows Subsystem for Linux (WSL): Powerful Tools and Practices for Cross-Platform Development and Collaboration](https://www.amazon.com/Hayden-Barnes-ebook/dp/B096TRZMW1)
- [Windows Subsystem for Linux 2 (WSL 2): Tips, Tricks and Techniques by Stuart Leeks](https://www.amazon.co.uk/Windows-Subsystem-Linux-Tricks-Techniques/dp/1800562446/)
- [Windows Subsystem for Linux: Tactics, Mindset and Tips](https://www.amazon.com/Windows-Subsystem-Linux-Tactics-Mindset/dp/1977718094)

## Additional Resources

- Microsoft [WSL Official Documentation](https://docs.microsoft.com/en-us/windows/wsl/)
- Microsoft [WSL Blog](https://blogs.msdn.microsoft.com/wsl)
- Microsoft [Console Blog](https://blogs.msdn.microsoft.com/commandline/)
- [WSL-Programs](https://github.com/ethanhs/WSL-Programs) - A community powered list of programs that work on the Windows Subsystem for Linux. ![github project][githublogo]
- [/r/bashonubuntuonwindows](https://www.reddit.com/r/bashonubuntuonwindows/) - Reddit subreddit.
- [##windows-wsl](https://irc-source.com/channel/freenode/%23%23windows-wsl) - IRC channel on Freenode.net. 
- [#debian-wsl](https://www.oftc.net) - IRC channel on OFTC.net.
- [WSL on GitHub](https://github.com/Microsoft/WSL) - For reporting issues with WSL. ![github project][githublogo]
- [Microsoft User Voice](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash) - Send Microsoft feedback on WSL.
- [Microsoft Developer Feedback](https://wpdev.uservoice.com/forums/266908-command-prompt-console-windows-subsystem-for-l) - For developers to send Microsoft feeback on WSL.
- [Portable Node.js guide](https://github.com/ehmicky/portable-node-guide) - Practical guide on how to write portable/cross-platform Node.js code.
- [Stack Overflow: WSL](https://stackoverflow.com/questions/tagged/wsl) - Programming question and answer site.

## Related Projects

- [Bash](https://www.gnu.org/software/bash/) - Bash is the GNU Project's shell. Bash is the Bourne Again SHell. Bash is an sh-compatible shell that incorporates useful features from the Korn shell (ksh) and C shell (csh).
- [Cygwin](https://cygwin.com) - Cygwin is a Unix-like environment and command-line interface for Microsoft Windows.
- [Cmder](https://cmder.net/) - A very nice console emulator built on ConEmu. ![github project][githublogo]
- [PuTTY](https://www.putty.org) - PuTTY is an SSH and telnet client, developed originally by Simon Tatham for the Windows platform. ![github project][githublogo]
- [PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/powershell-scripting?view=powershell-6) - PowerShell is a task automation and configuration management framework from Microsoft, consisting of a command-line shell and associated scripting language.
- [Visual Studio Code](https://code.visualstudio.com) - Visual Studio Code ("vscode") is a source code editor developed by Microsoft for Windows, Linux, and macOS. It includes support for debugging, embedded Git control, syntax highlighting, intelligent code completion, snippets, and code refactoring.
- [Visual Studio 2017](https://www.visualstudio.com/vs/) - Visual Studio is an IDE from Microsoft. It is used to develop computer programs, as well as web sites, web apps, web services and mobile apps. Visual Studio uses Microsoft software development platforms such as Windows API, Windows Forms, Windows Presentation Foundation, Windows Store, and Microsoft Silverlight.
- [Windows Services for UNIX](https://en.wikipedia.org/wiki/Windows_Services_for_UNIX) - SFU is a discontinued software package produced by Microsoft which provided a Unix environment on Windows NT and some of its immediate successor operating-systems. [TechNet](https://technet.microsoft.com/en-us/library/bb496506.aspx) documentation.

## More Awesome

- [Awesome UNIX](https://github.com/sirredbeard/Awesome-UNIX)
- [Awesome Windows](https://github.com/Awesome-Windows/Awesome)
- [Awesome VSCode](https://github.com/viatsko/awesome-vscode)
- [Awesome Bash](https://github.com/awesome-lists/awesome-bash)
- [Awesome Shell](https://github.com/alebcay/awesome-shell)
- [Awesome Powershell](https://github.com/janikvonrotz/awesome-powershell)
- [Awesome Linux](https://github.com/aleksandar-todorovic/awesome-linux)

More [![Awesome][awesomelogo]](https://awesome.re) lists. ![github project][githublogo]

## Thanks

- The Windows 10, WSL, and kernel teams at Microsoft, including but not limited to [Tara Raj](https://twitter.com/tara_msft), [Rich Turner](https://twitter.com/richturn_ms), [Jessie Frazelle](https://twitter.com/jessfraz), [Jack Hammons](https://github.com/jackchammons), [Sarah Cooley](https://github.com/scooley), [Ben Hillis](https://github.com/benhillis), [Allen Sudbring](https://blogs.technet.microsoft.com/askpfeplat/tag/allen-sudbring/), [Brandon Wilson](https://social.technet.microsoft.com/profile/BrandonWilson), [John Starks](https://twitter.com/gigastarks), [Russ Alexander](https://www.linkedin.com/in/russalex), [Yosef Durr](https://twitter.com/yosefdurr), [Sven Groot](https://twitter.com/svengroot_ms), [Sunil Muthuswamy](https://twitter.com/SunilMut), [Palkesh Soni](https://twitter.com/sonipalkesh), [John Starks](https://twitter.com/gigastarks), [Craig Wilhite](https://twitter.com/CraigWilhite).
- [Canonical](https://www.ubuntu.com), [Debian](https://www.debian.org), [SUSE](https://www.suse.com), and [Offensive Software](https://www.offensive-security.com).
- The [Awesome community](https://awesome.re) on GitHub.

## Intellectual Property Notices

- Linux® is a registered trademark of Linus Torvalds in the United States and/or other countries. [*](https://www.linuxfoundation.org/trademark-usage/)
- Windows®, Windows Server®, Windows 10®, Microsoft®, Microsoft Virtual Academy®, Visual Studio®, Azure®, PowerShell®, and MSDN® are trademarks or registered trademarks of Microsoft Corporation in the United States and/or other countries. [*](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general.aspx) [**](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/en-us.aspx)
- EdX® is a registered trademark of edX Inc. All Rights Reserved. [*](https://www.edx.org/trademarks)
- Ubuntu® and Canonical® are registered  trademark of Canonical Limited in the United States and/or other countries. [*](https://www.ubuntu.com/legal/terms-and-policies/intellectual-property-policy)
- SUSE® and SUSE Linux Enterprise® are registered trademarks of SUSE in the United States and/or other countries. [*](https://www.suse.com/company/legal/)
- Red Hat®, CentOS®, and Red Hat Enterprise Linux® are trademarks or registered trademarks of Red Hat, Inc. in the United States and/or other countries. [*](https://www.redhat.com/en/about/trademark-guidelines-and-policies)
- UNIX® is a trademark of The Open Group. Use of The Open Group trademarks are authorized by The Open Group Trademark Guidelines as "Editorial or Articles, but not Advertising" and/or permitted by trademark fair use under United States law. [*](http://www.unix.org/trademark.html)
- Debian® is a registered trademark of Software in the Public Interest, Inc. in the United States and/or other countries. [*](https://www.debian.org/trademark)
- Kali Linux® and Offensive Security® are registered trademarks of OffSec Services, Ltd. [*](https://www.offensive-security.com/trademark-policy/)
- Docker® and Docker Hub® are registered trademarks of Docker, Inc. [*](https://www.docker.com/trademark-guidelines)
- YouTube® is a registered trademark of Google, LLC. [*](https://www.google.com/permissions/trademark/our-trademarks.html)
- macOS® is a registered trademark of Apple, Inc. [*](https://www.apple.com/legal/intellectual-property/guidelinesfor3rdparties.html)
- GitHub® and [githublogo] are a registered trademarks of GitHub, Inc. [*](https://help.github.com/articles/github-terms-of-service/)
- Oracle and Oracle Linux are trademarks or registered tracemarks of Oracle, Inc. [*](https://www.oracle.com/legal/trademarks.html)
- Gentoo® is a trademark of the Gentoo Foundation, Inc. [*](https://www.gentoo.org/inside-gentoo/foundation/name-logo-guidelines.html)

All other trademarks mentioned herein are the property of their respective owners and may be registered in the United States and/or other countries.

The author of this project has no connection with Microsoft, Inc.

Portions of the descriptions above are from Wikipedia and used under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/). Portions of the descriptions above are from [Awesome-UNIX](https://github.com/sirredbeard/Awesome-UNIX) and used under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/).

This document is licensed under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/).

[githublogo]:https://raw.githubusercontent.com/sirredbeard/Awesome-WSL/master/github-icon.png
[awesomelogo]:https://awesome.re/badge.svg
