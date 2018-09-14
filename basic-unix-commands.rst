.. role:: bash(code)
   :language: bash


Basic Unix Commands
==============================================

=======================
The :bash:`man` command
=======================
This :bash:`man` command allows you to read the manual pages for a command. The manual page contains
the overview description of the comand, its command line arguments, and some example.

For example to get the manual page for :bash:`ls` command you can run,

.. code-block:: bash

   $ man ls

The manual pages can sometimes be hard to read, but they are available in every Linux or Unix-like machines.
However, you can also refer to `Devhint <https://devhints.io>`_ which is a quick reference for tools,
commands, and topics in computer science.

Many commands also have a help option that will give you some information. For example, with :bash:`ls`
you can run

.. code-block:: bash
   $ ls --help
   
The exact syntax will vary by command if available at all.

================================
:bash:`Ctrl+c` vs :bash:`Ctrl+z`
================================

:bash:`Ctrl+z` will suspend the program you are running (z like Zzz). On the other hand :bash:`Ctrl+c` will
stop the program you are running (e.g. program that stuck in infinite loop).

If you use :bash:`Ctrl+z` a lot and don't kill or restart the processes, you will end up with a lot of
processes just sitting there.

To restart a suspended process in the foreground, you can use the :bash:`fg` command. :bash:`bg` will restart
a process in the background.

=======
Listing
=======
To view the contents of the directory you are in, run :bash:`ls`. This is the most basic form of the command.

:bash:`ls -l`, shows more details, such as permissions size and the last time the files were edited. This will
be sorted by name. 

.. code-block:: bash

   $ ls -l
   total 19472
   -rw------- 1 krerkkiat krerkkiat  463097 Apr 19  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 1 (1).pptx
   -rw------- 1 krerkkiat krerkkiat  463097 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 1.pptx
   -rw------- 1 krerkkiat krerkkiat 1460689 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 2.pptx
   -rw------- 1 krerkkiat krerkkiat 1271326 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 3.pptx
   -rw------- 1 krerkkiat krerkkiat  984855 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 4.pptx
   -rw------- 1 krerkkiat krerkkiat  882673 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 1 (1).pptx
   -rw------- 1 krerkkiat krerkkiat  882673 Apr 12  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 1.pptx
   -rw------- 1 krerkkiat krerkkiat  955386 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 2(1).pptx
   -rw------- 1 krerkkiat krerkkiat  984164 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 3.pptx
   drwx------ 2 krerkkiat krerkkiat    4096 Apr  5  2017 circuit2 exam
   drwx------ 2 krerkkiat krerkkiat    4096 Apr  5  2017 Content
   -rw------- 1 krerkkiat krerkkiat 3614295 Apr 23  2017 EE2114 Final Review.pptx
   -rw------- 1 krerkkiat krerkkiat   22045 Jan 26  2017 EE2114 Syllabus - Spring 2017.docx
   drwx------ 6 krerkkiat krerkkiat    4096 Mar 19  2017 Labs
   -rw------- 1 krerkkiat krerkkiat 7074816 Mar 24  2017 Midterm2-Review.ppt

However, you can add :bash:`-rt` to it to sort the result by time and show the recent files on the bottom.

.. code-block:: bash

   $ ls -lrt
   total 19472
   -rw------- 1 krerkkiat krerkkiat   22045 Jan 26  2017 EE2114 Syllabus - Spring 2017.docx
   drwx------ 6 krerkkiat krerkkiat    4096 Mar 19  2017 Labs
   -rw------- 1 krerkkiat krerkkiat 7074816 Mar 24  2017 Midterm2-Review.ppt
   drwx------ 2 krerkkiat krerkkiat    4096 Apr  5  2017 circuit2 exam
   drwx------ 2 krerkkiat krerkkiat    4096 Apr  5  2017 Content
   -rw------- 1 krerkkiat krerkkiat  463097 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 1.pptx
   -rw------- 1 krerkkiat krerkkiat 1460689 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 2.pptx
   -rw------- 1 krerkkiat krerkkiat 1271326 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 3.pptx
   -rw------- 1 krerkkiat krerkkiat  984855 Apr 12  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 4.pptx
   -rw------- 1 krerkkiat krerkkiat  882673 Apr 12  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 1.pptx
   -rw------- 1 krerkkiat krerkkiat  984164 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 3.pptx
   -rw------- 1 krerkkiat krerkkiat  955386 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 2(1).pptx
   -rw------- 1 krerkkiat krerkkiat  882673 Apr 19  2017 Ch16_PPT_Fund_Elec_Circ_6e-Day 1 (1).pptx
   -rw------- 1 krerkkiat krerkkiat  463097 Apr 19  2017 Ch15_PPT_Fund_Elec_Circ_6e-Day 1 (1).pptx
   -rw------- 1 krerkkiat krerkkiat 3614295 Apr 23  2017 EE2114 Final Review.pptx
   
If you use :bash:`-a` it will show hidden files (these are files that start with a '.').

==================
Downloading a file
==================
:bash:`wget` or :bash:`curl` can be used to download a file to the remote server that you are connected to.
