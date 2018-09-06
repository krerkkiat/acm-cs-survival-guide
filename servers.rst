.. role:: bash(code)
   :language: bash

School Servers (or any server)
==============================================

===================
How many are there?
===================

There are many school servers that you can connect to, so you do not have to go to
the lab to do the assignment (some may argue that be in the lab also give the chance
to talk to other students; also you still have to go to the lab).

The list of the names can be obtain by go to `this page <http://ace.cs.ohio.edu/>`_.
Then you click on the "EECS Machine and services status pages". Browser will prompt
you to sign in, but you can just leave both fields blank. When you logged in, click on "Hosts"
on the sidebar will give you the liist of name of the server.

This list contains some other servers as well. The actual servers are prefixed with any of the
following.

* :bash:`odd`
* :bash:`sp-`
* :bash:`p`
* :bash:`pu`

Since all of these are with EECS department, so the full address have to be something similar
to the following.

* :bash:`odd15.cs.ohio.edu`
* :bash:`sp-003.cs.ohio.edu`
* :bash:`p1.cs.ohio.edu`
* :bash:`pu1.cs.ohio.edu`

======================
How to connect to one?
======================
On linux or MacOS you can open the terminal emulator, and type


=================
File Transferring
=================
There are serveral options to transfer the file from your laptop/pc to the servers.

---------
FileZilla
---------


---------
Cyberduck
---------
`Cyberduck <https://cyberduck.io/>`_ is a file transferring tool that also have support for other cloud storage services.


-------------------
:bash:`scp` command
-------------------
Typical command that should be avaiable on most of the Unix-like system.
This command though can overwrite the file, so be careful with it.
More information can be found using :bash:`man scp` command.

The following example is to transfer file from local machine to the server.

:bash:`scp ./project1.cc bobcat@odd15.cs.ohio.edu:/home/bobcat/project1.cc`
