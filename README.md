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

Linux is a [UNIX-like](https://github.com/sirredbeard/Awesome-UNIX#frequently-asked-questions) [open-source](https://opensource.org/osd) operating system developed by Linus Torvalds.

### What is a Linux distribution?

Linux alone is just a kernel, the piece of the operating system that lies between the hardware and the applications you run. When people 'run Linux' they are running a Linux distribution. A Linux distribution is a collection of all the applications required to boot, use, and modify Linux, such as a shell for commands, an editor for editing files, and other basic operating system utilities. Unlike Windows there are many different Linux distributions, each of which is assembled by a different community, company, or person with a specific goal in mind. The goal of the Debian Project is to produce a universal operating system. There are also Linux distributions based on other distributions. Ubuntu is a distribution based on Debian built 

### What is Windows?

Windows is a family of proprietary operating systems, all of which are developed, marketed, and sold by Microsoft. Windows Subsystem for Linux first shipped in Windows 10 Anniversary Update, version number 1607, in August 2016. WSL can be enabled on all versions of Windows after 1607, including Home, Professional, Enterprise, Server, and Education.

### What is the Windows Subsystem for Linux?

Windows Subsystem for Linux is a compatibility layer for running Linux binary executables natively on Windows 10. WSL provides a Linux-compatible kernel interface developed by Microsoft, which can then run a Linux userland of the users choice on top of it. It is the successor to defunct [Windows Services for UNIX](https://en.wikipedia.org/wiki/Windows_Services_for_UNIX).

### How does Windows Subsystem for Linux work?

* [Windows Subsystem for Linux Overview](https://blogs.msdn.microsoft.com/wsl/2016/04/22/windows-subsystem-for-linux-overview/) at MSDN. 
* [Additional articles](https://blogs.msdn.microsoft.com/wsl/) at MSDN regarding the technical underpinnings of WSL.
* [Windows Subsystem for Linux Documentation](https://docs.microsoft.com/en-us/windows/wsl/about) from docs.microsoft.com.

### How do I install the Windows Subsystem for Linux?

* [Windows 10 Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10) - Microsoft's official documentation.
* [Windows-Subsystem-For-Linux-Setup](https://github.com/michaeltreat/Windows-Subsystem-For-Linux-Setup) - A basic guide for how to get setup with the WSL feature that is included with Windows 10. ![github project][githublogo]

### What can I do with Windows Subsystem for Linux?

WSL is undoubtedly a tool for power users, developers, and UNIX/Linux geeks who want to run Windows. Most of the things you can do with WSL are going to be related to programming, automation, and other geeky things.

#### WSL-Specific

* [Everything You Can Do With Windows 10’s New Bash Shell](https://www.howtogeek.com/265900/everything-you-can-do-with-windows-10s-new-bash-shell/)
* [Epic Development Environment using Windows Subsystem for Linux](https://medium.com/@johnwoodruff91/epic-dev-environment-with-wsl-dc81e234ae61)
* [Setting Up a Programming Environment via Windows 10 Bash](https://www.cs.odu.edu/~zeil/FAQs/Public/win10Bash/)

#### WSL Command Line Skills

* [The Unix Workbench](http://seankross.com/the-unix-workbench/) - A book for anyone to get started with Unix/Linux.
* [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line) - Master the command line in one page. ![github project][githublogo]
* [The Bash Academy](http://www.bash.academy) - The Bash Academy is an initiative to promote the bash shell language and educate people on its use.
* [Awesome Command Line Apps](https://github.com/herrbischoff/awesome-command-line-apps) [![Awesome][awesomelogo]](https://awesome.re) ![github project][githublogo]

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

* [Windows Store](https://www.microsoft.com/store/productId/9NBLGGH4MSV6) for Ubuntu 16.04
* [Windows Store](https://www.microsoft.com/store/productId/9N9TNGVNDL3Q) for Ubuntu 18.04
* [Installing Software](https://help.ubuntu.com/community/InstallingSoftware) from Ubuntu

### Debian

Debian is a Linux distribution assembled by the non-profit [Debian](https://www.debian.org/) Project.

* [Windows Store](https://www.microsoft.com/store/productId/9MSVKQC78PK6)
* [Package Management](https://www.debian.org/doc/manuals/debian-reference/ch02.en.html) from Debian

### OpenSUSE

OpenSUSE is a Linux distribution produced by [SUSE Linux GmbH](https://www.opensuse.org/) and other companies. Leap 42 is a community-produced distribution with more recent software. SUSE Enterprise Linux is an enterprise-grade commercial distribution with tested software.

* [Windows Store](https://www.microsoft.com/store/productId/9NJVJTS82TJX) for Leap 42
* [Windows Store](https://www.microsoft.com/store/productId/9P32MWBH6CNS) for SUSE Enterprise Linux
* [Zypper](https://en.opensuse.org/Portal:Zypper) package manager from SUSE

### Kali Linux

Kali Linux is a Linux distribution focused on penetration testing based on Debian that is produced by [Offensive Security](https://www.kali.org/).

* [Windows Store](https://www.microsoft.com/store/productId/9PKR34TNCV07)

# Unofficial Distributions

Unofficial distributions must be installed manually or with tools listed below. They are not available in the Windows Store.

* [miniwsl](https://github.com/0xbadfca11/miniwsl) - A mini Linux distribution for WSL powered by [busybox](https://www.busybox.net/).
* [WSL-Distribution-Switcher](https://github.com/RoliSoft/WSL-Distribution-Switcher) - Scripts to replace the distribution behind WSL with any other Linux distribution published on [Docker Hub](https://hub.docker.com/explore/). Includes alpine, CentOS, Fedora, Clear, and others. ![github project][githublogo]

# WSL Tools

### Terminals

* [wsltty](https://github.com/mintty/wsltty) - Mintty as a terminal for WSL. ![github project][githublogo]
* [wsl-terminal](https://github.com/goreliu/wsl-terminal) - A terminal emulator for WSL, based on mintty, fatty and wslbridge. ![github project][githublogo]
* [ConEmu](https://conemu.github.io) - ConEmu aims to be handy, comprehensive, fast and reliable terminal where you may host any console application for the Windows command line, PowerShell, or WSL. 

### Other

* [LxRunOffline](https://github.com/DDoSolitary/LxRunOffline) - A full-featured utility for WSL. ![github project][githublogo]
* [wslgit](https://github.com/andy-5/wslgit) - Use git installed WSL from Windows and Visual Studio Code (VSCode). ![github project][githublogo]
* [VcXsrv](https://sourceforge.net/projects/vcxsrv/) - X server for Windows. Required for running Linux GUI apps in Windows.

# Additional WSL Resources

* [The Windows Subsystem for Linux Guide](http://wsl-guide.org/en/latest/)
* [WSL-Programs](https://github.com/ethanhs/WSL-Programs) - A community powered list of programs that work on the Windows Subsystem for Linux. ![github project][githublogo]
* [WSL-DistroLauncher](https://github.com/Microsoft/WSL-DistroLauncher) - Reference launcher app for developing your own WSL distribution Microsoft Store packages. ![github project][githublogo]

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
