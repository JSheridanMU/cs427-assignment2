# CS427 Assignment 2

## Introduction

In this assignment, you will be working on the provided `ipynb` notebook, 
where you will fill in necessary pieces of code to complete the general stereo pipeline. 
Follow the instructions below to get started. **Note that the versions of packages etc. that are 
used are quite specifics.** We have included a 
[Troubleshooting](#troubleshooting) section at the bottom of the page where we will add any common
problems (& solutions) as we become aware of them.

## Setup
1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html). Choose your OS, Architecture and Python 3.8. _Skip this step if you have anaconda or miniconda already installed with Python 3.5+_
1. Create a conda environment, using the following command. On Windows, open the installed **Conda Prompt** (or **Anaconda Prompt**) to run this command. On MacOS and Linux, you can just use a **terminal** window to run the command.: `conda create -n cs427_hw2 "python>=3.6,<3.7"`. Confirm the packages marked for installation if prompted.
1. This should create an environment named `cs427_hw2`. Activate it using `conda activate cs427_hw2`.
1. Then navigate to your projects directory (or create one) and then do `git clone https://gitlab.cs.nuim.ie/cs427_2021/students/assignment2`
1. `cd` into the `assignment2` folder 
1. Now install requirements using `pip install -r requirements.txt`
1. Run the notebook using: `jupyter lab`
1. Then open the browser using the link displayed in the output of the jupyter lab command 
or open your browser and go to `http://localhost:8888`, you'll have to paste the token from the output. 

For convenience, here are all the commands
```sh
conda create -n cs427_hw2 "python>=3.6,<3.7" --yes
conda activate cs427_hw2

mkdir projects
cd projects
git clone https://gitlab.cs.nuim.ie/cs427_2021/students/assignment2
cd assignment2
pip install -r requirements.txt
jupyter lab
```

## Getting familiar with notebooks

For learning purposes, we suggest you create a new notebook and try out some basic python commands.

Notebooks are made up of cells. There are two modes
- Command Mode <kbd>Esc</kbd> (text cursor is not visible, for executing shortcuts)
- Cell Mode <kbd>Enter</kbd> (text cursor is visible, for typing code)

The following shortcuts are the most used ones and can be executed from any mode.
Run Cell Ctrl Enter
Run Cell and go to next cell Shift Enter

You can also search for actions on the sidebar when you press <kbd>Crtl</kbd><kbd>Shift</kbd><kbd>C</kbd> 
and then execute, for example, `Run all cells`

Commands like `Cut` `Copy` `Paste` for _text_ works usual inside text mode once text is selected.
Commands for `Cut` `Copy` `Paste` for _cells_ work when you are on Command Mode
with <kbd>X</kbd>, <kbd>C</kbd> and <kbd>V</kbd> respectively
 
Also, in command mode, insert new cell above with <kbd>A</kbd> and below with <kbd>B</kbd> doing any rough calculations. 
Once you are done, you can delete the current cell with <kbd>D</kbd><kbd>D</kbd> (again, in command mode) 
 
Video Tutorial below
 
[![Jupyterlab Tutorial Video](https://i.imgur.com/jkiUkN7.png)](https://youtu.be/pxirOmilQ3A)
 
If you feel even more adventurous, you can read more [here](https://jupyterlab.readthedocs.io/en/stable/user/interface.html#keyboard-shortcuts).
 
 

## Coding and Submission guidelines

- Open [exercise.ipynb](exercise.ipynb)
- Read the instructions and fill out necessary code.
- Before submission `Restart Kernel and Run All Cells`, 
check if all cells got executed with output and save the notebook.

You should submit your work as a by saving and uploading your completed [exercise.ipynb](exercise.ipynb) file through 
the [moodle submision link](https://2020.moodle.maynoothuniversity.ie/mod/assign/view.php?id=137568). When submitting, ensure that you
- do not have cells that display outputs more than a page long, for e.g. printing out all elements of an image array.
- have not added external files or loaded them in the notebook.
- have not used any other libraries/code that provide functionality to produce desired output. e.g. `from skimage.measure import ransac`

## Troubleshooting

- `conda create` fails on Windows. _Solution_: It may fail if you use a normal command prompt. Use _Anaconda Prompt_.
- `pip` is not recognised as an internal or external command. _Solution_: Run `conda install pip -y` in your environment.
- Jupyter lab fails when selecting the python kernel with and error that ends with: `ImportError: DLL load failed while importing win32api: The specified module could not be found.` _Solution_: Run `conda install pywin32`
