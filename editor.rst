.. role:: bash(code)
   :language: bash

Editors
==============================================
Here are some well known editors.

============
Command line
============
These will be come in handy if you are perform quick editing on the server.
You will usually be told to use :bash:`nano`, but you also have the following option.

* :bash:`nano`
   A simple lightweight text editor.

* :bash:`micro`
   A simple lightweight text editor written in Go. It is focused on being intuitive. More information
   can be found at `https://micro-editor.github.io/ <https://micro-editor.github.io/>`_. :bash:`micro` is not installed
   by default on the school servers, but you can quickly download the prebuilt binary and run it as follow.

   .. code-block:: bash
   
      $ wget https://github.com/zyedidia/micro/releases/download/v1.4.1/micro-1.4.1-linux64.tar.gz
      $ tar -xf micro-1.4.1-linux64.tar.gz
      $ ./micro-1.4.1/micro

* :bash:`emacs`
   This editor is a little more complex to use at first, but is significantly more powerful than the two above.

* :bash:`vim`
   Like :bash:`emacs` this editor is one of the more complicated to learn, but is also very powerful.
   If you want to get a quick start in customizing you Vim editor, `Vim Bootstrap <https://vim-bootstrap.com/>`_ is
   a really good place to start.

===
GUI
===
* `VS Code <https://code.visualstudio.com/>`_
   Microsoft's cross-platform text editor. It has a `set of extensions <https://visualstudio.microsoft.com/services/live-share/>`_ that allow users to remotely collaborate on the project. 
* `Atom <https://atom.io/>`_
   Popular cross-platform text editor. This editor also have functionality that is similar to the live collaboration of VS Code. More information can be found `here <https://teletype.atom.io/>`_.
* `Sublime Text <https://www.sublimetext.com/>`_
   Popular cross-platform text editor.
* `Notepad++ <https://notepad-plus-plus.org/>`_
   Popular free text editor for Windows.
* `Geany <https://www.geany.org/>`_
   It is the light-weight editor.
* Gedit
   This should be installed on the workstation.
  
All of these text editors (except for Notepad++) are available in Linux repositories.

===============
Tips and Tricks
===============

One quick note on line numbers. Most of editors will turn on line numbers by default for you.
However Gedit does not, but you can turn them on via :bash:`Edit->Preferences`.
On :bash:`vim` you can use the :bash:`:set number` command to show line numbers or :bash:`:set nonumber` to turn them off.

If you ever accidentally start :bash:`vim` you can quit without saving by typing :bash:`ESC:q!`.

If you ever accidentally start :bash:`emacs` you can quit without saving by typing :bash:`Ctrl-x Ctrl-c`

If you write code on Windows and then copy the code to a Linux system, you will find the '^M' character at the end of every line.
To remove these characters, you can run :bash:`sed -i 's/\r//g filename'` in the directory with the file.
To prevent this from happening, you can go into your editor's settings and change the line ending type from Windows to UNIX.
