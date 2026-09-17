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

This repo
