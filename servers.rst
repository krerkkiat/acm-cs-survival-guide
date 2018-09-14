.. role:: bash(code)
   :language: bash

School Servers
==============================================

===================
How many are there?
===================

The school has multiple servers available for EECS students to connect to. These servers
make it possible for you to work on homework in your dorms or at home without needing
access to a Linux distro on your computer. That said, sometimes it is useful to go to
the labs to avoid distractions.

There is a list of the servers available at `this page <http://ace.cs.ohio.edu/>`_.
Just click on the "EECS Machine and services status pages". Your browser will prompt
you to sign in, but you can just leave both fields blank. When you "logged in", click
on "Hosts" on the sidebar to get the list of all the servers.

This list contains some other servers as well. The most useful servers are prefixed with any of the
following.

* :bash:`odd` These are the Ubuntu machines in the computer lab.
* :bash:`sp-` These are more of the Ubuntu machines in the computer lab.
* :bash:`p` These are the old Solaris machines. You will only rarely use these.
* :bash:`pu` They are Ubuntu machines that has the same setup as the lab workstations.
* :bash:`tesla2` This is a special Ubuntu machine with CUDA that can be used for machine learning.

Since all of these are with the EECS department the full address will be something similar to the following:

* :bash:`odd15.cs.ohio.edu`
* :bash:`sp-003.cs.ohio.edu`
* :bash:`p1.cs.ohio.edu`
* :bash:`pu1.cs.ohio.edu`
* :bash:`tesla2.cs.ohio.edu`

These servers all keep your home folder on a network filesystem, so all your files will be accessible
on any of them (including the Solaris servers).

As a small note, there is a :bash:`tesla1` machine, however students do not have access to it.

======================
How to connect to one?
======================
On Linux or MacOS you can open the terminal emulator, and type

.. code-block:: bash

   $ ssh odd15.cs.ohio.edu
   
On Windows, the easiest way is to use puTTY. You can save your sessions with it to quickly
connect to various servers as needed.

=================
File Transferring
=================
There are serveral options to transfer the file from your laptop/pc to the servers.

---------
WinSCP
---------
This is a file transferring tool that is part of the puTTY project. It will have access to your saved puTTY sessions, so you do not need to create new sessions for this tool.

---------
FileZilla
---------
A popular free to use file transferring tool.

---------
Cyberduck
---------
`Cyberduck <https://cyberduck.io/>`_ is a file transferring tool that also has support for other cloud storage services.


-------------------
:bash:`scp` command
-------------------
This is a common command that should be avaiable on most Unix-like systems.
This command can overwrite files, so be careful with it.
More information can be found using :bash:`man scp` command.

The following example is to transfer file from local machine to the server.

.. code-block:: bash

   $ scp ./project1.cc bobcat@odd15.cs.ohio.edu:/home/bobcat/project1.cc

The following example is to transfer a folder (recursively) from remote machine to the local machine.

.. code-block:: bash

   $ scp -r bobcat@odd15.cs.ohio.edu:/home/bobcat/cs2400/project1/ ./project1/

=====================
Note on other servers
=====================
If you have access to servers other than the school servers, all of the aforementioned information
is also applicable.

Just use the hostname or public IP address of that server instead of the school servers.
