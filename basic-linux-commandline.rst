.. role:: bash(code)
   :language: bash


Basic Unix Commands
==============================================

================================
:bash:`Ctrl+c` vs :bash:`Ctrl+z`
================================

:bash:`Ctrl+z` is pausing the program your are running (z like Zzz). On the other hand :bash:`Ctrl+c` is
stopping the program you are running (e.g. program that stuck in infinite loop).

If the :bash:`Ctrl+z` is used a lot, you will end up with a lot of program in the background.

=======
Listing
=======
The obvious one is :bash:`ls`. It list the files and folder of the current working directory.

:bash:`ls -l`, however, will shows more detail. This will be sorted by name. 

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

==================
Downloading a file
==================
:bash:`wget` or :bash:`curl` can be used to download a file to the remote server that you are connected to.

