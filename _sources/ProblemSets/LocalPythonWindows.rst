.. _Windows_Setup:

Using Python Locally: Windows
-----------------------------

It's time to get Python running independently on your own computer! This will require some setup along with learning some new things about your computer, such as how to use a command line interface.

If that sounds intimidating, don't worry. While learning to use the command line can seem scary, it's not bad at all if you learn it in steps and practice regularly. Before you know it, you'll find interacting with your computer via the command line super useful and even fun!

Getting Familiar with the Command Line
======================================

Before we install Python on our computers, let's get familiar with the command line.

Install Git for Windows
***********************

The first step is to install Git for Windows so that you can use Git Bash as your command line interface. We want to use this instead of Powershell, because Git Bash uses UNIX commands which are used on Linux and OSX command lines as well. Additionally, we'll use Git extensively later in the course.

Download `Git for Windows`_. Once you have downloaded it, you can open Git Bash to use the shell.

Practice the command line
*************************

We're going to use Appendix A from the online book *Learn Python the Hard Way* (don't worry, the book is more approachable than it sounds). This section is called `Command Line Crash Course`_ and it contains 15 short tutorials teaching you the basics of how to interact with your computer's file and operating systems using a "terminal" or "shell". **Do not follow the instructions for Windows**. Follow the instructions for Linux/OSX instead, since Git Bash uses UNIX commands. Do all 15 lessons **EXCEPT lesson 12**, which teaches commands that do not work in Git Bash.

Installing and Running Python Locally
=====================================

By "locally" we mean that you are now about to install and run Python directly on your computer, as opposed to through some web-based or remote tool.

Install a code editor
*********************

First, we'll install Visual Studio Code, a general-purpose code editor that features a Python debugger. The steps to do this are:

1. Go to `Visual Studio Code`_ and select the Windows platform to download (it should automatically feature *Download for Windows* and you can click that green button to download, otherwise select "installer" next to Windows after clicking the green dropdown arrow).
#. Double click the downloaded file and follow the installer instructions (the default selections are fine).
#. Open Visual Studio Code and click "View", then "Extensions". In the Extensions menu that will appear, you'll see an option named "Python" with a subheader of "Linting, Debugging(multi-threaded...)". Click the green "Install" button for this extension.

Install Miniconda Python 3
**************************

Now let's install Python 3 using Miniconda. Follow these steps:

1. Go to Conda_ and download the Miniconda "Python 3.6" Windows 64-bit installer (Note: the version may have changed since the time of this writing; just make sure to select the latest version of Python beginning with "3.").
#. When you open the installer for Miniconda, after agreeing to the terms, you'll see a screen that says "Install for: ". Select the button that says "All Users" and then click "Next" to carry on with the installation process.
#. Verify that Python 3 installed correctly by opening Git Bash and typing ``python -V``. It should print to the screen the version of Python you just installed.
#. Now, open Git Bash and enter the following commands into your shell: ``cd ~`` and press Enter, and then ``touch .bashrc`` and press Enter, and then ``start .bashrc`` and press Enter. The ``.bashrc`` file will open in a text editor. Enter this line into the file exactly as it appears: ``alias python='winpty python.exe'`` then save and close the file. Back on the command line, enter ``source .bashrc`` and press Enter.

Make Your First Local Python Program
====================================

Follow these steps to get your first Python program up and running on your computer:

1. Make a directory to store your Python code on your computer using Git Bash.

   a) Make sure you are in your home directory with the command ``cd ~``
   #) Make a new directory named "lc101": ``mkdir lc101``
   #) Move into that directory: ``cd lc101``

#. Enter your Python code and run it.

   a. Create a file in that directory named "hello.py": ``touch hello.py``
   #. Open your "lc101" directory in the Visual Studio Code editor from Git Bash with the command: ``code .``
   #. In your code editor, open ``hello.py`` and type ``print("Hello, World!")``. Then save the file (you can use the shortcut ``ctrl + S``).
   #. Back in Git Bash, run the program by typing ``python hello.py``. You should see "Hello, World!" appear (without the quotes).

**Congratulations on running your first python program locally!!**

.. _Git for Windows: https://git-for-windows.github.io
.. _Command Line Crash Course: http://learnpythonthehardway.org/book/appendixa.html
.. _Visual Studio Code: https://code.visualstudio.com
.. _Conda: https://conda.io/miniconda.html