# Data Analysis Environment Setup — macOS

This guide will help you set up the development environment you will use throughout the **Marcy Lab School Data Analytics Fellowship**.

No prior experience setting up a Python development environment is required. Follow the steps **in order**, and do not skip the verification steps.

## What You Will Set Up

By the end of this guide, your Mac will have:

* **Git** — used to download and manage code
* **Miniconda** — used to manage Python and Python environments
* **Python 3.13**
* **VS Code** — the code editor we will use
* **Jupyter** — used to run Python notebooks
* Common data analysis libraries such as:

  * pandas
  * NumPy
  * Matplotlib
  * Seaborn
  * scikit-learn
  * statsmodels
  * Plotly

---

## Before You Start

You will use the **Terminal** several times during setup.

The Terminal lets you give your computer commands using text instead of clicking through menus.

### Open Terminal

1. Press **Command + Space** to open Spotlight Search.
2. Type:

```text
Terminal
```

3. Press **Enter**.

You should see a window containing a command prompt.

> **Important:** Only type the commands shown inside the code blocks. You do not need to type the `$` symbol if you see it in another tutorial.

---

## Step 1: Check Git

Git is used to download this repository and will be used throughout the fellowship.

In Terminal, run:

```bash
git --version
```

### If Git Is Installed

You should see something similar to:

```text
git version 2.x.x
```

Your exact version may be different.

Continue to **Step 2**.

### If Git Is Not Installed

Your Mac may prompt you to install the **Command Line Developer Tools**.

Follow the installation prompts.

After installation finishes, close and reopen Terminal and run:

```bash
git --version
```

again.

Do not continue until this command returns a Git version.

---

## Step 2: Install Miniconda

### What Is Miniconda?

Python projects often need different versions of Python and different packages.

**Conda** helps us manage these environments.

Think of a Conda environment as a separate workspace containing the exact Python version and packages needed for a project.

We will use **Miniconda**, which provides Conda without installing a large number of extra packages that we do not need.

### Download Miniconda

Go to the official Miniconda installation page:

https://www.anaconda.com/docs/getting-started/miniconda/install

Choose the installer for **macOS**.

Your Mac will normally use one of two processor types:

* **Apple Silicon** — M1, M2, M3, M4, M5, etc.
* **Intel** — older Macs

### Not Sure Which Mac You Have?

1. Click the **Apple menu** in the top-left corner.
2. Select **About This Mac**.
3. Look for **Chip** or **Processor**.

If you see something such as:

```text
Apple M3
```

you have an **Apple Silicon Mac**.

If you see:

```text
Intel
```

you have an **Intel Mac**.

Download the appropriate Miniconda installer and follow the installation instructions.

---

## Step 3: Verify Conda

After installing Miniconda, **close Terminal completely and reopen it**.

Then run:

```bash
conda --version
```

You should see something similar to:

```text
conda 25.x.x
```

Your version may be different.

If you see a Conda version, continue.

### If You See `conda: command not found`

First:

1. Close Terminal.
2. Reopen Terminal.
3. Run:

```bash
conda --version
```

again.

If Conda still cannot be found, return to the Miniconda installation instructions and verify that installation completed successfully.

---

## Step 4: Clone This Repository

### What Does "Clone" Mean?

Cloning creates a copy of a GitHub repository on your computer.

In Terminal, run:

```bash
git clone https://github.com/The-Marcy-Lab-School/data-analysis-environment-macOS.git
```

Then move into the new folder:

```bash
cd data-analysis-environment-macOS
```

### Verify That You Are in the Correct Folder

Run:

```bash
pwd
```

The path should end with:

```text
data-analysis-environment-macOS
```

You can also run:

```bash
ls
```

You should see files including:

```text
README.md
environment.yaml
```

---

## Step 5: Create Your Data Analysis Environment

This repository contains a file called:

```text
environment.yaml
```

This file tells Conda which version of Python and which packages to install.

Run:

```bash
conda env create -f environment.yaml
```

Conda will begin downloading and installing Python and the required packages.

This may take several minutes.

> **Important:** Do not close Terminal while the environment is being created.

---

## Step 6: Activate the Environment

After installation finishes, activate the environment:

```bash
conda activate data-analysis-env
```

Your Terminal prompt should now include:

```text
(data-analysis-env)
```

For example:

```text
(data-analysis-env) yourname@MacBook %
```

This tells you that the environment is active.

---

## Step 7: Verify Python

Run:

```bash
python --version
```

You should see:

```text
Python 3.13.x
```

The final number may be different depending on the latest compatible Python 3.13 release.

For example:

```text
Python 3.13.7
```

### If You Do Not See Python 3.13

Stop here.

Make sure your environment is active:

```bash
conda activate data-analysis-env
```

Then check again:

```bash
python --version
```

---

## Step 8: Verify Your Conda Environment

Run:

```bash
conda env list
```

You should see `data-analysis-env` in the list.

The active environment will have an `*` next to it.

For example:

```text
base
data-analysis-env    *
```

---

## Step 9: Install VS Code

### What Is VS Code?

**Visual Studio Code (VS Code)** is the code editor we will use throughout the fellowship.

Download VS Code from:

https://code.visualstudio.com/

Install the macOS version.

After installation, open **Visual Studio Code**.

---

## Step 10: Install the Required VS Code Extensions

In VS Code:

1. Click the **Extensions** icon on the left side of the window.
2. Search for:

```text
Python
```

3. Install the **Python extension published by Microsoft**.
4. Search for:

```text
Jupyter
```

5. Install the **Jupyter extension published by Microsoft**.

These extensions allow VS Code to work with Python files and Jupyter notebooks.

---

## Step 11: Open the Repository in VS Code

You can open the repository directly from Terminal.

First, make sure you are inside the repository:

```bash
cd data-analysis-environment-macOS
```

Make sure your environment is active:

```bash
conda activate data-analysis-env
```

Then run:

```bash
code .
```

The `.` means:

> Open the folder I am currently inside.

### If `code .` Does Not Work

Open VS Code manually.

Then select:

**File → Open Folder**

Find and select:

```text
data-analysis-environment-macOS
```

---

## Step 12: Select Your Python Interpreter

VS Code needs to know which Python installation it should use.

We want it to use the Python installation inside:

```text
data-analysis-env
```

In VS Code:

1. Press **Command + Shift + P**.
2. Search for:

```text
Python: Select Interpreter
```

3. Select the interpreter associated with:

```text
data-analysis-env
```

It should indicate that it is using **Python 3.13**.

> **Important:** Do not select `base` if `data-analysis-env` is available.

---


# Setup Complete

You now have the core development environment needed for the Data Analytics Fellowship.

You have successfully set up:

* Git
* Miniconda
* Python 3.13
* `data-analysis-env`
* VS Code
* Python VS Code extension
* Jupyter VS Code extension
* Core Python data analysis packages
* Jupyter notebooks

---

# A Common Production Workflow

**Setup only happens once.**

You do **not** need to reinstall everything every time you want to write Python.

When you return to your work on another day, your workflow will usually look something like this.

## 1. Open Terminal

Open Terminal using Spotlight:

**Command + Space → Terminal**

## 2. Navigate to Your Project

Use `cd` to move into the folder containing your project.

For example:

```bash
cd path/to/your/project
```

Your actual path will depend on where your project is stored.

## 3. Activate Your Environment

Run:

```bash
conda activate data-analysis-env
```

Look for:

```text
(data-analysis-env)
```

at the beginning of your Terminal prompt.

## 4. Open VS Code

From your project folder, run:

```bash
code .
```

## 5. Work on Your Project

You can now work with:

* `.py` Python files
* `.ipynb` Jupyter notebooks
* Git
* GitHub
* your installed data analysis libraries

## 6. When You Are Finished

You can deactivate the environment:

```bash
conda deactivate
```

---

# Troubleshooting

Environment setup problems are normal.

Read the error message carefully before changing or reinstalling anything.

## Problem: `conda: command not found`

Try closing Terminal completely and reopening it.

Then run:

```bash
conda --version
```

If Conda still cannot be found, verify that Miniconda was installed successfully.

---

## Problem: `git: command not found`

Run:

```bash
git --version
```

macOS may prompt you to install the Command Line Developer Tools.

Complete the installation and try again.

---

## Problem: My Terminal Says `(base)`

You may see:

```text
(base)
```

at the beginning of your Terminal prompt.

This means Conda is installed, but you are currently using Conda's default environment.

Activate the fellowship environment:

```bash
conda activate data-analysis-env
```

Your prompt should change to:

```text
(data-analysis-env)
```

---

## Problem: I Am Using the Wrong Python Version

First check:

```bash
python --version
```

If you do not see Python 3.13, check which environment is active:

```bash
conda env list
```

Then activate the correct environment:

```bash
conda activate data-analysis-env
```

Check again:

```bash
python --version
```

---

## Problem: VS Code Cannot Find `data-analysis-env`

First activate the environment in Terminal:

```bash
conda activate data-analysis-env
```

Then open VS Code from that Terminal:

```bash
code .
```

Inside VS Code:

1. Press **Command + Shift + P**.
2. Select **Python: Select Interpreter**.
3. Look for `data-analysis-env`.

---

## Problem: My Notebook Says "Select Kernel"

Click **Select Kernel** in the top-right corner of the notebook.

Select the Python environment associated with:

```text
data-analysis-env
```

Do not select another Python installation unless your instructor tells you to.

---

## Problem: `EnvironmentNameNotFound`

If you run:

```bash
conda activate data-analysis-env
```

and Conda says the environment does not exist, check your environments:

```bash
conda env list
```

If `data-analysis-env` is missing, return to the repository folder and run:

```bash
conda env create -f environment.yaml
```

---

## Problem: The Environment Already Exists

If Conda tells you:

```text
prefix already exists
```

or that `data-analysis-env` already exists, **do not create another copy**.

Check your environments:

```bash
conda env list
```

Then try:

```bash
conda activate data-analysis-env
```

---

## Problem: Environment Creation Failed

First make sure you are in the repository:

```bash
pwd
```

Then check that `environment.yaml` exists:

```bash
ls
```

You should see:

```text
environment.yaml
```

Try the environment creation command again:

```bash
conda env create -f environment.yaml
```

Read the error message carefully if it fails again.

---

# Starting Over

Do not remove your environment unless you actually need to start over.

If instructed to completely rebuild the environment, first deactivate it:

```bash
conda deactivate
```

Then remove it:

```bash
conda env remove -n data-analysis-env
```

Verify that it is gone:

```bash
conda env list
```

Then recreate it from the repository:

```bash
conda env create -f environment.yaml
```

Activate it:

```bash
conda activate data-analysis-env
```

And verify Python:

```bash
python --version
```

You should see:

```text
Python 3.13.x
```

---

# Important Reminders

* **Do not install random Python packages globally.**
* Use the `data-analysis-env` Conda environment for fellowship Python work.
* Activate your environment before running Python code.
* Make sure VS Code is using the `data-analysis-env` interpreter.
* Make sure Jupyter notebooks are using the `data-analysis-env` kernel.
* Read Terminal error messages before trying random fixes.
* Do not delete and reinstall your entire environment as your first troubleshooting step.
* If you are unsure about an error, save or copy the **entire error message** so that you can share it with your instructor.

## Quick Reference

Check Git:

```bash
git --version
```

Check Conda:

```bash
conda --version
```

Activate your environment:

```bash
conda activate data-analysis-env
```

Check Python:

```bash
python --version
```

See your Conda environments:

```bash
conda env list
```

Open the current folder in VS Code:

```bash
code .
```

Deactivate your environment:

```bash
conda deactivate
```

---

**You are ready to begin working with Python for data analysis.**

