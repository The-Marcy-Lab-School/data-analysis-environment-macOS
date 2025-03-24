# Setting Up a Python Environment for Data Analysis on macOS with VS Code

This guide will walk you through setting up a Python environment for data analysis on macOS using VS Code. We'll utilize a provided `environment.yaml` file to create a Conda environment, and ensure you have the necessary VS Code extensions installed.

## Prerequisites

* **VS Code:** Ensure you have VS Code installed on your macOS system. If not, download and install it from [https://code.visualstudio.com/](https://code.visualstudio.com/).
* **Anaconda or Miniconda (Recommended):** Conda is a package and environment manager that simplifies the process of creating and managing Python environments. If you don't have it, we recommend installing Miniconda (a minimal installer) from [https://docs.conda.io/en/latest/miniconda.html](https://docs.conda.io/en/latest/miniconda.html). Follow the macOS installation instructions.

## Steps

1.  **Clone this Repository:**

    * Clone this repository to your local machine. Replace `<repository_url>` with your repository's URL and navigate inside the repo.

        ```bash
        git clone <repository_url>
        cd <repository_directory>
        ```



2.  **Create the Conda Environment:**

    * Use the `conda env create` command with the `environment.yaml` file to create the environment.

        ```bash
        conda env create -f environment.yaml
        ```

    * This command will create a Conda environment named `data-analysis-env` (as specified in your `environment.yaml`) and install all the packages listed in the file.

3.  **Open the Project in VS Code:**

    * Open VS Code and navigate to the directory containing the repository that you cloned down you should be INSIDE the repository (using "File" -> "Open Folder...".

4.  **Select the Conda Environment in VS Code:**

    * Open the Command Palette in VS Code by pressing `Cmd + Shift + P`.
    * Type "Python: Select Interpreter" and press Enter.
    * VS Code should detect the `data-analysis-env` environment. Select it from the list. If it doesn't appear, you may need to restart VS Code.

5.  **Install the Python and Jupyter Extensions:**

    * In VS Code, go to the Extensions view by clicking the Extensions icon in the Activity Bar (the square icon on the left side of the VS Code window).
    
    * Search for "Python" and install the Microsoft Python extension.
    * Search for "Jupyter" and install the Microsoft Jupyter extension.
    * These extensions provide essential features for Python development and Jupyter Notebook support in VS Code.

6.  **Verify the Environment:**

    * Create a new Python file (e.g., `test.py`) or a Jupyter Notebook file (`.ipynb`).
    * In the Python file, add a simple print statement:

        ```python
        print("Python environment setup successful!")
        ```

    * Run the Python file by right-clicking in the editor and selecting "Run Python File in Terminal".
    * In a Jupyter Notebook, run a simple cell to verify the environment is working.

7.  **Using the Jupyter Notebook:**

    * If you created a `*.ipynb` file, VS Code should automatically use the Jupyter extension to render it.
    * Make sure that the correct kernel is selected in the top right corner of the notebook. The kernel should correspond to your `data-analysis-env` environment. If not, select it from the kernel dropdown.
    * Run a simple python cell to verify that the environment is working.

## Troubleshooting

* **Environment Not Found:** If VS Code doesn't detect the `data-analysis-env` environment, ensure that Conda is correctly installed and that the environment was created successfully. You might need to restart VS Code.
* **Package Installation Issues:** If you encounter issues during the `conda env create` step, check your internet connection and ensure that the `environment.yaml` file is correctly formatted.
* **Kernel Issues:** if the jupyter notebook kernel is not correct, select the correct kernel from the dropdown in the upper right hand corner of the notebook.
* **Conda not found:** If conda commands are not found, make sure that the conda install location is in your PATH environment variable.
