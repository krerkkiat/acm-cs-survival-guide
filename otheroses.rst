
Running other OSes
==============================================
Many of you have Windows or macOS installed, but will want
access to Linux on your own personal systems for development.
There are two major options, using a virtual machine, or
dual-booting.

===============
Virtual Machine
===============
A virtual machine allows your computer to run a second
operating system inside of your primary OS. Most
virtual machine offerings will not perform as well as
having Linux installed natively, but many people feel
more comfortable doing this than dual booting. There
are many options, so try out a few of them and see
which one works best for you. Of the following four
options, all but one will work on any host OS.

----------
VirtualBox
----------
A popular and free "general-purpose full virtualizer for x86 harware, targeted at server, desktop and embedded use".

----
QEMU
----
A free as in speech emulator. It is capable of emulating multiple architecture types, including x86, x86_64, and MIPS. It does not come with a GUI, but there are some that are available for it.

-------
Hyper-V
-------
A hypervisor built into Windows Professional, Education, and Enterprise editions. It performs very well if you have access to it.

------
VMware
------
A free (but not open source) virtualizer for x86 hardware.

=========
Dual Boot
=========
Some of the previous graduates found that they preferred
to having Linux run natively for better performance, or
because virtualization just did not work well on their
systems due to old hardware. Systems with a dual boot
set up can boot more than one OS. When set up properly
a Linux boot loader will appear when turning on the
computer and allows the user to pick between Windows and
Linux, or macOS and Linux at boot time.

Modern Linux distros such as Ubuntu and Fedora include
installers capable of setting up your system to have more
than one OS installed. They will automatically shrink your
Windows partition, and create new partitions on your
hard drive that will contain Linux. Try out a LiveUSB and
make sure your hardware will work with Linux before you
install Linux.
