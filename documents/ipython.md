# iPython

## What is it?

Powerful interactive Python shell

- tab completion
- extensible 'magic' commands for controlling environment and performing many Python AND OS tasks
- ability to edit multi-line cell blocks
- syntax highlighting

You can use it as a more robust interactive Python shell, or combine it with scripts to do analytics or debugging.

## Usage

### Installation

Should come with conda installation, but otherwise use `conda install ipython` or `pip install ipython`

### Magic Commands

Magic commands are basically enhancements to normal Python code that help simplify or solve common problems with a handy "magic" command. They can run external code files, interact and modify your shell environment, or perform Python tasks. There are two flavors of magic commands: with a % prefix or with a %% prefix.  % prefix represents that the command operates over a single line of code whereas %% prefix allows the command to operate over an entire cell. 

Here are some magic commands that I find particularly useful:

**Running External Files**

- `%run` run any python script and load into current

**Perform Python Tasks**

- `%whos` see all variables
- `%timeit` gets execution time of Python statement or expression
- `%debug` enter debugging mode
- `%matplotlib` can show plots with matplotlib

**Perform OS Tasks**

- `%cd` change directory
- `%ls` see files in current directory
- `%pwd` return the current working directory path