# Environment Set-up

For CS375, we highly recommend that you use your own personal machine with a Mac or Linux operating system.
 
- *Rationale:* Having your own machine will make it easy for us to help you during office hours. Additionally, we will be using Jupyter Notebooks in a browser which have a bit more complicated set-up if you were to use the Williams CS machines. 

We (the TAs and instructor) will not be supporting Windows machines. 

If you do not own your own machine or you are having technical issues with a machine you own, the following two resources may be helpful 

1. [Williams financial aid support for computer purchases](https://www.williams.edu/sfs/current-student-faqs/)
1. [Short-term 2-week laptop loans from the library](https://libguides.williams.edu/c.php?g=916778&p=853068)

Complete the following four parts to ensure that your environment is set-up correctly for the assignments in the remainder of the course. 

## Part 1: Installing Miniconda 

### 1. Miniconda installation 

We will use [miniconda](https://docs.conda.io/en/latest/miniconda.html) to install Python and related packages.

Navigate to [miniconda installer webpage](https://docs.anaconda.com/miniconda/). We are using "Conda 24.7.1 Python 3.12.4 released Aug 22, 2024". 

Download the install that matches your machine's OS (and chips for Apple machines). For a Mac, you can look this up by choosing the Apple logo in the top left of the screen and then choose `About this Mac`. 

Note: If you already have an anaconda or miniconda installation, it may be helpful to uninstall those versions and reinstall fresh to make sure you have the correct version numbers. 

### 2. After miniconda installation 

After installation, close and reopen your terminal. If you installed miniconda correctly, you should now see `(base)` at the beginning of your shell prompt. 

Run the following command to make sure you installed the version of conda you intended to: 

```
conda -V 
```

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

1. Let's create a conda environment with the necessary dependencies. 

	Note, you should run the following commands in the directory containing `environment.yml` (e.g. the directory `hw0-preliminaries` which you should already be in after completing the steps in Part 2 of these instructions). 

	```
	conda  env create -f environment.yml
	```
	
	This will create a new Python environment -- you can think of this as a separate, clean installation of Python that we can install packages in without messing with any existing Python setup you may have. Then it will look up all of the packages in `environment.yml`, go to the internet and download them, and then install them in the environment. If those packages require any other packages for them to work, it will also install those.

	Open the `environment.yml` file and you can see the various package versions we will be using in this class. Note, we are using `Python 3.11`. 
	
	Note that this downloading and installation process may take a few minutes, that's entirely normal.

1. Activate the newly created environment:

	```
	conda activate cs375
	```
	You should now see `(cs375)` at the beginning of your shell prompt. You'll need to run `conda activate cs375` every time you open a new terminal and re-start your notebook server.

## Part 4: Jupyter notebooks 

1. Within the same repo, start your jupyter notebook server by typing the command

	```
	jupyter notebook
	```

1. A window should open automatically in your default browser. If it does not, the terminal output should contain a URL you can use to open the notebook in a browser of your choice.

1. From the Jupyter notebook file explorer window that opens, click on the `jupyter_tutorial.ipynb` or `python_tutorial.ipynb` files to open them. 





