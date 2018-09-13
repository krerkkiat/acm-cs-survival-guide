.. role:: bash(code)
   :language: bash

Editors
==============================================
These are a list of some well known editors.

============
Command line
============
These will be come in handy if you are perform quick editing on the server.
You will usually be told to use :bash:`nano`, but you also have the following option.

* :bash:`nano`

  * A simple lightweight text editor.
* :bash:`micro`

  * A simple lightweight text editor.
* :bash:`emacs`

  * This editor is a little more complex to use at first, but is significantly more powerful than the two above
* :bash:`vim`

  * Like :bash:`emacs` this editor is one of the more complicated to learn, but is also very powerful.

:bash:`micro` is not installed by default on the school servers, but you can install it
only for your user.

===
GUI
===
* `VS Code <https://code.visualstudio.com/>`_

  * Microsoft's cross-platform text editor.
* `Atom <https://atom.io/>`_

  * Popular cross-platform text editor.
* `Sublime Text <https://www.sublimetext.com/>`_

  * Popular cross-platform text editor.
* `Notepad++ <https://notepad-plus-plus.org/>`_
project1.cc
  * Popular free text editor for Windows.
* `Geany <https://www.geany.org/>`_

  * It is the light-weight editor.
* Gedit

  * This should be installed on the workstation.
  
All of these text editors (except for Notepad++) are available in Linux repositories.

===============
Tips and Tricks
===============

One quick note on line number. Most of the editor will turn on the line number by default for you.
However, Gedit is not, so you can turn in on via :bash:`Edit->Preferences`.
On :bash:`vim` you can use :bash:`set number` to show line number or :bash:`set nonumber` to turn it off.

If you write code on Windows and then copy the code to a Linux system, you will find the '^M' character at the end of every line.
To remove these characters, you can run :bash:`sed -i 's/\r//g filename'` in the directory with the file.
To prevent this from happening, you can go into your editor's settings and change the line ending type from Windows to UNIX.
