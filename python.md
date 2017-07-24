# Setting up Python

A lot of people have trouble setting up python. Either you go for the lightweight option and installing everything leads you to dependency hell. Or you pick a complete distribution which is bloated with packages you will probably never use. This document aims to be a guide to get to a reliable python setup for beginners. 

Until you're a little more experienced with how python works, downloading python from it's official website is not recommended. The package manager that ships with this version of python is called pip and can sometimes be problematic when dependency issues arise. 

For beginners, Anaconda is a good place to start. Anaconda is a python distribution that's maintained by Continuum Analytics. It comes with it's own package manager called conda which is easier to use than pip. However, the basic anaconda installer comes with all sorts of packages which you don't need yet. 

There happens to be a more lightweight version of Anaconda called Miniconda (also official). This comes with just the python interpreter and the conda package manager. This is what we will be installing. 

Download the required version from [here](https://conda.io/miniconda.html). We recommend python 3.6.

Go through the installer for your operating system. Instructions are available [here](https://conda.io/docs/install/quick.html).

Make sure you enable "Add Anaconda to my PATH variable" and make Anaconda your default python distribution. While these are not necessary, this should work quite well unless you install another python distribution. The windows installer is shown below. Make sure you check both these options. 

![Add to PATH](http://i.imgur.com/Qd0TMxO.png)

Once the installation is complete, we should test out our installation. To try out python enter `python` on cmd/PS/terminal. You should get a prompt like the following

```
Python 3.6.0 |Continuum Analytics, Inc.| (default, Dec 23 2016, 11:57:41) [MSC v.1900 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>

```
The `>>>` part should have a blinking cursor. This is the python REPL( Read-Evaluate-Print-Loop ) prompt. You can type in commands here and see the results. Try ` print('Hello, world!') ` and press Enter. If everything goes fine, ``` Hello, world! ``` should be printed on the next line. To exit the prompt, press Ctrl+Z and then Enter on Windows and Ctrl/Cmd+D on macOS/linux.

Next we should install some of the packages you'll be needing. Make sure you're connected to the internet.

1. Open up the Command Prompt/PowerShell/Terminal( macOS and linux). 
2. type `conda install numpy scipy matplotlib jupyter notebook` and press enter( To be able to run conda from anywhere, it needs to be present in the PATH environment variable, hence the need to check the option during installation )
3. Wait for all the packages to be downloaded and installed. On linux and macOS it may ask for the root password. 

To check if all packages have been installed, type ` conda list ` at the command line. It will output the list of packages. If numpy, scipy and jupyter are listed, then we're all set up. 

