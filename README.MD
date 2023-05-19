[![Build Status](https://travis-ci.org/joommf/conda-install.svg?branch=master)](https://travis-ci.org/joommf/conda-install)

# STEP 1
## conda install

Jupyter OOMMF can be installed via conda. The basic steps are:

- install Anaconda (use "miniconda" if you are short of disk space). See for example https://docs.anaconda.com/anaconda/install/ for details

- run the following command to install Jupyter OOMMF

<pre>
    conda install -c conda-forge oommfc
</pre>


- you will also want to install the Jupyter Notebooks
<pre>
    conda install notebook
</pre>

  and maybe other python packages you want to use.


We are working on a conda package with name 'joommf' which will
install the notebook automatically.


## Which version of OOMMF is provided?

On Linux and OS X, the conda-forge install (as described above) provides oommfc compile from the sources available in http://github.com/fangohr/oommf/ . These include the bulkDMI OOMMF extension.

On Windows, the conda-forge install (as describe above) provides the OOMMF as is distributed from NIST (see https://github.com/conda-forge/oommf-feedstock/blob/master/recipe/meta.yaml#L10).



# STEP 2

## Managing conda
Verify that conda is installed and running on your system by typing:

		conda --version
Conda displays the number of the version that you have installed. You do not need to navigate to the Anaconda directory.

EXAMPLE: conda 4.7.12

### Note

If you get an error message, make sure you closed and re-opened the terminal window after installing, or do it now. Then verify that you are logged into the same user account that you used to install Anaconda or Miniconda.

Update conda to the current version. Type the following:

		conda update conda
Conda compares versions and then displays what is available to install.

If a newer version of conda is available, type y to update:

		Proceed ([y]/n)? y
#### Tip

We recommend that you always keep conda updated to the latest version.

## Managing environments
Conda allows you to create separate environments containing files, packages, and their dependencies that will not interact with other environments.

When you begin using conda, you already have a default environment named base. You don't want to put programs into your base environment, though. Create separate environments to keep your programs isolated from each other.

1. Create a new environment and install a package in it.

We will name the environment snowflakes and install the package BioPython. At the Anaconda Prompt or in your terminal window, type the following:

		conda create --name snowflakes biopython
Conda checks to see what additional packages ("dependencies") BioPython will need, and asks if you want to proceed:

		Proceed ([y]/n)? y
Type "y" and press Enter to proceed.

2. To use, or "activate" the new environment, type the following:

Windows: conda activate snowflakes

macOS and Linux: conda activate snowflakes

#### Note

conda activate only works on conda 4.6 and later versions.

For conda versions prior to 4.6, type:

Windows: activate snowflakes

macOS and Linux: source activate snowflakes

Now that you are in your snowflakes environment, any conda commands you type will go to that environment until you deactivate it.

3. To see a list of all your environments, type:

		conda info --envs
A list of environments appears, similar to the following:

	conda environments:

    base           /home/username/Anaconda3
    snowflakes   * /home/username/Anaconda3/envs/snowflakes
#### Tip

The active environment is the one with an asterisk (*).

4. Change your current environment back to the default (base): conda activate

#### Note

For versions prior to conda 4.6, use:

Windows: activate

macOS, Linux: source activate

#### Tip

When the environment is deactivated, its name is no longer shown in your prompt, and the asterisk (*) returns to base. To verify, you can repeat the conda info --envs command.

# Managing Python
When you create a new environment, conda installs the same Python version you used when you downloaded and installed Anaconda. If you want to use a different version of Python, for example Python 3.6, simply create a new environment and specify the version of Python that you want.

1. Create a new environment named "snakes" that contains Python 3.6:

		conda create --name snakes python=3.6
When conda asks if you want to proceed, type "y" and press Enter.

2. Activate the new environment:

Windows: conda activate snakes

macOS and Linux: conda activate snakes

#### Note

conda activate only works on conda 4.6 and later versions.

For conda versions prior to 4.6, type:

Windows: activate snakes

macOS and Linux: source activate snakes

3. Verify that the snakes environment has been added and is active:

		conda info --envs
Conda displays the list of all environments with an asterisk (*) after the name of the active environment:

## conda environments:
#
base                     /home/username/anaconda3
snakes                *  /home/username/anaconda3/envs/snakes
snowflakes               /home/username/anaconda3/envs/snowflakes
The active environment is also displayed in front of your prompt in (parentheses) or [brackets] like this:

		(snakes) $
4. Verify which version of Python is in your current environment:

		python --version
5. Deactivate the snakes environment and return to base environment: conda activate

Note

For versions prior to conda 4.6, use:

Windows: activate

macOS, Linux: source activate



# STEP 3: 

## Install some libraries

		$ pip install -r requirement.txt



# STEP 4: 
## Run Jupyter Notebook


This command is going to start the local server so that we can access Jupyter using the browser. Jupyter may also automatically open after running the command below in the command prompt. 

    $ jupyter-lab

If Jupyter does not automatically open in your browser, please go ahead and copy one of the URLs at the bottom of the text generated after running the launch command.

This will open a window that is shown below in the browser. In this case, JupyterLab has been set to a dark theme, however, it may also open in white mode which can be changed under the setting menu

To proceed we need to click on Python 3 which is the first tab on this window. 

This will open a new Python notebook which is a new ipynb file named untitled since we’re yet to save it. So this gives us access to all the cells where we can start to write our Python code.

## Coding


Suppose we create a simple variable x and initialize it with a value of 5. To run the variable we need to hit the run button.  

Now that the variable has been created in the notebook, we can access it by simply typing the name of the variable in any of the cells.

We can also delete cells by right-clicking on the cell that we intend to delete and selecting the delete option.  

Besides this, we can also write codes that span over more than one line and still run them in the same way. For instance, we can create a list that spans over multiple lines.

Now using a for loop we can also iterate over the list as we would in a normal IDE such as VS Code and the code works just fine. In this case, the code for the for loop need not be in the same cell as the list.
