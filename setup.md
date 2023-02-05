# Environment Set-up

For CS375, we highly recommend that you use your own personal machine with a Mac or Linux operating system.
 
- *Rationale:* Having your own machine will make it easy for us to help you during office hours. Additionally, we will be using Jupyter Notebooks in a browser which have a bit more complicated set-up if you were to use the Williams CS machines. 

We (the TAs and instructor) will not be supporting Windows machines. 

If you do not own your own machine or you are having technical issues with a machine you own, the following two resources may be helpful 

1. [Williams financial aid support for computer purchases](https://www.williams.edu/sfs/current-student-faqs/)
1. [Short-term 2-week laptop loans from the library](https://libguides.williams.edu/c.php?g=916778&p=853068)

Complete the following four parts to ensure that your environment is set-up correctly for the assignments in the remainder of the course. 

## Part 1: Installing Miniconda 

### 1A. Own Machine (recommended)

We will use [miniconda](https://docs.conda.io/en/latest/miniconda.html) to install Python and related packages.

We require `Python 3.8`. Be sure that you install the Python 3.8 version and not the latest Python version. This is the version of Python other packages depend on.  

#### Mac 
Navigate to [this section of the miniconda installer webpage](https://docs.conda.io/en/latest/miniconda.html#macos-installers). 

If you have an Intel chip download: 
```
Python 3.8 > Miniconda3 macOS Intel x86 64-bit pkg
```

If you have a M1 chip download: 
```
Python 3.8 > Miniconda3 macOS Apple M1 ARM 64-bit pkg
```

#### Linux 

Navigate to [this section of the miniconda installer webpage](https://docs.conda.io/en/latest/miniconda.html#linux-installers). 

Download 
```
Python 3.8 > Miniconda3 Linux 64-bit
```


### 1B. Williams CS machines (not recommended)

We DO NOT recommend using Williams machines for this class. We will be using Jupyter Notebooks extensively and setting these up to interact with ssh is a bit more complicated. However, we provide instructions here for extenuating circumstances. 

Instructions for Williams VPN and the ssh servers available are on [this page](https://www.cs.williams.edu/systems/). If you forgot your password and need to reset, please email Lida Doret (lpd2@williams.edu). 

Steps: 

1. If not connected to the network, log into your VPN
	2. Log into a compute server available from off campus, e.g.
	```
	ssh jcool@lohani.cs.williams.edu
	```
3. Run the following commands in the terminal to update bash settings and use conda

	```
	cd /usr/cs-local/c375_katie
	./c375_bashrc_update.sh
	```
4. Logout
5. Log Back In


On the Williams servers, this version of miniconda lives in 
```
/etc/miniconda3/bin/conda
```
You con confirm this by typing this command on the command line: 
```
which conda
```

### 2. After Conda installation 
After you have installed conda (on any machine), open a terminal and run the following command to see the conda version 

```
conda -V 
```
Your conda version should be equal to or greater than `22.11.0`. 


## Part 2: Git set-up  

This assignment, and all of the future ones, will be distributed as a git repository.

Git set-up: 

1. Make sure git is set-up on your local machine. 

2. Open the terminal and find a suitable folder to clone the assignment repo. Go there with cd:
	
	```
	cd /folder/to/put/cs375/assignments/
	```
	Note: You should replace `/folder/to/put/cs375/assignments/` with your folder's name. 

3. From there, clone the assignment via

	```
	git clone https://github.com/cs375williams/hw0-preliminaries.git
	```

4. Move to that directory 

	```
	 cd hw0-preliminaries
	```

## Part 3: Creating a Conda environment 

1. Create a conda environment with the necessary dependencies. Note, you should run the following commands in the directory containing `environment.yml` (e.g. the directory `hw0-preliminaries` which you should already be in after completing the steps in Part 2 of these instructions):

	```
	conda env create -f environment.yml
	```
	
	This will create a new Python environment -- you can think of this as a separate, clean installation of Python that we can install packages in without messing with any existing Python setup you may have. Then it will look up all of the packages in `environment.yml`, go to the internet and download them, and then install them in the environment. If those packages require any other packages for them to work, it will also install those.
	
	Note that this downloading and installation process may take a few minutes, that's entirely normal.

1. Activate the newly created environment:

	```
	conda activate cs375
	```
	You should now see `(cs375)` in front of your shell prompt. You'll need to run `conda activate cs375` every time you open a new terminal and re-start your notebook server.

## Part 4: Jupyter notebooks 

1. Within the same repo, start your jupyter notebook server by typing the command

	```
	jupyter notebook
	```

1. A window should open automatically in your default browser. If it does not, the terminal output should contain a URL you can use to open the notebook in a browser of your choice.

1. From the Jupyter notebook file explorer window that opens, click on the `jupyter_tutorial.ipynb` or `python_tutorial.ipynb` files to open them. 





