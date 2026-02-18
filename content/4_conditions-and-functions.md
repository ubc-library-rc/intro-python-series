---
layout: default
title: 4 Using Conditions and Writing Functions
nav_order: 18
---

# Workshop 4 - Using Conditions and Writing Functions

## Workshop goal

To learn to use logic and modularity to make code flexible and reusable.

## Episodes and questions

### 4.1 Making Decisions with Conditional Statements
- How can my programs do different things based on data values?


### 4.2 Creating Functions
- How can I define new functions?
- What’s the difference between defining and calling a function?
- What happens when I call a function?
- How do I work with variables inside and outside of functions?
- How do I make sure my functions are doing what I want?
- How do I use docstrings to make my functions more usable?

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