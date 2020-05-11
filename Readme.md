
# Implementing a planning search

This is the second project of Artificial Intelligence Nanodegree at Udacity, aiming to solve deterministic logistics planning problems for an Air Cargo transport system using a planning search agent.

***Note:** Read Chapter 10 of "Artificial Intelligence: A modern Approach" 3rd edition by Peter Norvig on planning available [here](AIMA-3rd-ed.pdf) before starting this project.*

## Setting up Anaconda environment

***(Note: The Recommended Python Version by Udacity is 3.5 or 3.6)***

#### 1. Download the AIND Anaconda environment

Enter the following command in your Linux terminal:
```
wget https://video.udacity-data.com/topher/2018/May/5afdeed0_aind-universal-v3/aind-universal-v3.yml
```

or directly download for windows from [here](aind-universal-v3.yml).

*(Note for Windows users: Some browsers will automatically append a ".txt" extension to the yml file; if your browser does this, then you will need to remove the extension or alter the creation command to correct it.)*

#### 2. Create the environment

Open a Conda activated terminal or Anaconda Prompt and run:

```
conda env create -f aind-universal-v3.yml
```

#### 3. Activate the Environment

- Windows: `activate aind`
- Linux/Mac: `source activate aind`

##### Installation Errors

*WARNING: SOME OPERATING SYSTEMS MAY PRODUCE ERRORS WHILE INSTALLING Z3 -- DO NOT PANIC.*

It can be challenging to configure Z3, particularly on some versions of Windows. You may use the information below to attempt installing Z3 on Windows, but that platform is not well-supported by the Z3 library maintainers.

NOTE: You may need a C/C++ compiler to build some of the required packages if your system cannot find an installable binary. OSX & Linux users can use gcc & g++/clang *(OSX users will need the XCode Command Line Tools available by running `xcode-select --install` from a Terminal.)* Windows users can download & install Visual C++ Build Tools [here](http://landinghub.visualstudio.com/visual-cpp-build-tools).

Activate the conda environment (source activate aind or activate aind, depending on your OS), then try installing with pip:

```
pip install z3-solver
```