.. _getting_started:

===============
Getting started
===============

Here you will find the basics to work with Scicluster.
Please read the links at the end of each paragraph for more detailed information.

Get an account
--------------

If you are associated with the Faculty of Science, Ferdowsi University of Mashhad, you may apply locally.

Connect to Scicluster
-----------------

You may connect to Scicluster via *SSH* to ``172.21.127.53``.
This means that on Linux and OSX you may directly connect by opening a terminal and writing ``ssh username@172.21.127.53``.
From Windows, you may connect via PuTTY software. X-forwarding for graphical applications is not possible currently.
Please see the following link for details to all mentioned methods. :doc:`/account/login`

On nodes and files
------------------

When you login, you will be on the frontend node. Please do *not* run any long-lasting programs here.
The frontend should only be used for job preparation (see below) and simple file operations.

You will also be in your home directory ``/home/username``. Here, you have ... GB at your disposal without backup.
For actual work, please use the work area at ``/work8/``. It is better to make a directory with your username as

::

 mkdir /work8/username

This space is also not backed up, but it has a good performance and is 8 TB in size. Please remove old files regularly. :doc:`/storage/storage`

To move files from your computer to Scicluster or vice versa, you may use any tool that works with *ssh*. On Linux and OSX, these are scp, rsync, or similar programs. On Windows, you may use WinSCP.

Run a program
-------------

There are many programs and libraries pre-installed. You may get a list of all programs by typing ``module avail``.
When you found your program of choice, you may load it using ``module load``. You can also compile your own software, if necessary. :doc:`/software/modules`

To eventually run the program, you have to write a job script. In this script, you can define how long the job (i.e. the program) will run and how much memory and compute cores it needs. For the actual computation, you need to learn at least the basics of Linux shell scripting.

When you wrote the job script, you can start it with ``sbatch jobscript.sh``.
This will put the script in the queue, where it will wait until an appropriate compute node is available.
You can see the status of your job with ``squeue -u username``. :doc:`/jobs/batch` and :doc:`/jobs/examples`

Get help
--------

Do you need help with Scicluster? Write us an email to .... You can also request new software (either an update or entirely new software), suggest changes to this documentation, or send us any other suggestions or issues concerning Scicluster to that email address. Please also read the rest of this documentation.

Happy computing!
