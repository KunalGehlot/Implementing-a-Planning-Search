
# Implementing a planning search  <!-- omit in toc --> 

This is the second project of Artificial Intelligence Nanodegree at Udacity, aiming to solve deterministic logistics planning problems for an Air Cargo transport system using a planning search agent.

***Note:** Read Chapter 10 of "**Artificial Intelligence: A modern Approach**" 3rd edition by Peter Norvig on planning available [here](AIMA-3rd-ed.pdf) before starting this project.*

Find the official Readme for the project [here](default%20instructions.md)

## Index  <!-- omit in toc --> 

- [Setting up Anaconda environment](#setting-up-anaconda-environment)
    - [1. Download the AIND Anaconda environment](#1-download-the-aind-anaconda-environment)
    - [2. Create the environment](#2-create-the-environment)
    - [3. Activate the Environment](#3-activate-the-environment)
      - [Installation Errors](#installation-errors)
    - [4. Installing `pypy`](#4-installing-pypy)
    - [5. Run test](#5-run-test)
- [Exercise Details](#exercise-details)
  - [Example Problem](#example-problem)
  - [Test](#test)
    - [Running the test](#running-the-test)
- [Results](#results)
  - [Find the Results here](#find-the-results-here)


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

#### 4. Installing `pypy`

`pypy` is an alternative to the standard `cPython`  runtime that tries to optimize and selectively compile your code for improved speed, and it can run 2-10x faster for this project. There are binaries available for Linux, Windows, and OS X. Simply download and run the appropriate `pypy` binary installer *(make sure you get version 3.5)* or use the package manager for your OS. When properly installed, any `python` commands can be run with `pypy` instead. (*You may need to specify `pypy3` on some OSes.)*

```
conda install pypy3
```

#### 5. Run test

After completing the code, run
```
pypy3 -m unitttest -v
```

## Exercise Details

### Example Problem

Run the example problem *(based on the cake problem from Fig 10.7 in Chapter 10.3 of [AIMA](AIMA-3rd-ed.pdf))*

```
pypy3 example_have_cake.py
```

### Test

The run_search.py script allows you to choose any combination of eleven search algorithms (*three uninformed and eight with heuristics)* on four air cargo problems. The cargo problem instances have different numbers of airplanes, cargo items, and airports that increase the complexity of the domains.

You should run all of the search algorithms on the first two problems and record the following information for each combination:

- Number of actions in the domain
- Number of new node expansions
- Time to complete the plan search

Use the results from the first two problems to determine whether any of the uninformed search algorithms should be excluded for problems 3 and 4. You must run at least one uninformed search, two heuristics with greedy best first search, and two heuristics with A* on problems 3 and 4.

#### Running the test

To run the test, enter:
```
pypy3 run_search.py -m
```

To select the problems and search algorithm inline, enter the problem and search number separated by spaces like this:
```
pypy3 run_search.py -p 1 2 3 -s 1 2 3 4 5
```

## Results

### Find the Results [here](report.md)

The file `report.pdf` includes all of the figures (charts and tables) and written responses to the questions below.

1. Use a table or chart to analyze the number of nodes expanded against number of actions in the domain
2. Use a table or chart to analyze the search time against the number of actions in the domain
3. Use a table or chart to analyze the length of the plans returned by each algorithm on all search problems
4. Use your results to answer the following questions:

    - Which algorithm or algorithms would be most appropriate for planning in a very restricted domain (i.e., one that has only a few actions) and needs to operate in real time?

    - Which algorithm or algorithms would be most appropriate for planning in very large domains (e.g., planning delivery routes for all UPS drivers in the U.S. on a given day)

    - Which algorithm or algorithms would be most appropriate for planning problems where it is important to find only optimal plans?


<!-- ![Progression air cargo search](/images/Progression.PNG) -->

