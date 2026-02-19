---
layout: default
title: 5 Good Habits when Programming for Research
nav_order: 22
---

# 5 Good Habits when Programming for Research

## Workshop goal

To develop good habits for programming for research, including handling errors, debugging, and writing reliable code.

## Episodes and questions

### 5.1 Errors

- How does Python report errors?
- How can I handle errors in Python programs?

### 5.2 Writing reliable code

- How can I make my programs more reliable?

### 5.3 Debugging

- How can I fit testing into my programming habits/workflow?
- How can I debug my program?

## Setup

These instructions assume you've already installed the required software for this workshop series (instructions in [Introduction and Setup](./0_introduction.md)).

If you have not finished the installation requirements, you can write code here: [https://mybinder.org/v2/gh/koudyk/blank-python-notebook/HEAD?urlpath=%2Fdoc%2Ftree%2Findex.ipynb](https://mybinder.org/v2/gh/koudyk/blank-python-notebook/HEAD?urlpath=%2Fdoc%2Ftree%2Findex.ipynb)

1. Create a project folder where you'll store data and Python scripts, or find the folder you used in previous workshops in this series.
2. [Download this file](https://github.com/ubc-library-rc/intro-python-series/blob/main/content/book-data.zip), un-zip it, and put it in the folder you just created.
3. To open your project in VS Code, open VS code, select `File > Open Folder`, and open the folder with the data.

### Create a local Python environment, if you haven't in a previous workshop

Skip this step if you created a Python environment for the previous workshop.

Best practice in Python is to create a **virtual environment** for each project, which contains all the specific libraries (and specific versions) that you need for that project.

We will use the `venv` tool to create an environment with the following steps:
1. Open the Command Palette with `Ctrl+Shift+P`
2. Type in **Python: Create Environment** and click on it
3. Select `venv` as the tool we want to use to create the environment
4. Select the Python interpreter that you want to use (probably the one with the highest numbers, starting with something like `Python 3.10`)

After following these steps,  VS Code will create a `.venv` folder in your project folder.

### Activate the environment

VS Code may give you a pop-up asking if you want to activate the virtual environment that you just created.
If it does, select Yes.

If not, you can run a command in the terminal (in VS Code) to activate it.

For **Windows**, you should run `.venv\Scripts\activate`.

For **Mac** or **Linux**, you should run `source .venv/bin/activate`

### Install Python libraries

In the terminal in VS Code, you can install the libraries that we will need for this workshop by running the following commands.

First, if you just created your Python environment, you should upgrade `pip`, which is the tool that we use to install Python libraries.

```bash
pip install --upgrade pip
```

Now we can install the libraries `numpy` and `matplotlib`.

```bash
pip install numpy matplotlib
```

## Acknowledgements

These materials borrow heavily from the ["Programming with Python" materials by Software Carpentry](https://swcarpentry.github.io/python-novice-inflammation/), which is available under a [CC-BY 4.0 license](https://swcarpentry.github.io/python-novice-inflammation/LICENSE.html).