Here is a complete, beginner-friendly `README.md` file. It walks students through the entire process from scratch—installing Python, choosing an IDE, setting up a virtual environment, installing dependencies, and running the notebook.

You can save this text as `README.md` in the same folder as your notebook and `requirements.txt`.

***

# Introductory Machine Learning Lab — Setup Guide

Welcome to your first Machine Learning lab! This guide will walk you through everything you need to do to get your computer ready, from zero to running your first Jupyter Notebook. 

Follow these steps in order. Don't rush—you only have to do this setup once!

---

## Step 1: Install Python

Python is the programming language we will use. 

1. Go to the official Python website: [python.org/downloads](https://www.python.org/downloads/)
2. Click the big button to download the latest version of Python (version 3.10 or newer).
3. Open the installer you just downloaded.
4. **⚠️ CRITICAL STEP FOR WINDOWS USERS:** At the very bottom of the installer window, check the box that says **"Add python.exe to PATH"**. If you skip this, your computer won't know where Python is!
5. Click **Install Now** and wait for it to finish.

**Verify the installation:**
1. Open your computer's terminal:
   * **Windows:** Press the `Windows` key, type `cmd`, and press Enter.
   * **Mac:** Press `Command + Space`, type `Terminal`, and press Enter.
2. Type the following command and press Enter:
   ```bash
   python --version
   ```
   *(If you are on a Mac, you might need to type `python3 --version`)*. If you see a version number (like `Python 3.12.2`), you are good to go!

---

## Step 2: Install an IDE (VS Code)

An IDE (Integrated Development Environment) is the app you use to write code. We strongly recommend **Visual Studio Code (VS Code)** because it is free, lightweight, and handles Jupyter Notebooks beautifully.

1. Go to the VS Code website: [code.visualstudio.com](https://code.visualstudio.com/)
2. Download the version for your operating system (Windows, Mac, or Linux).
3. Run the installer and accept all the default settings.

**Install the Jupyter Extension for VS Code:**
1. Open VS Code.
2. On the left side of the screen, click the **Extensions** icon (it looks like 4 square blocks).
3. In the search bar, type `Python` and click **Install** on the one made by Microsoft.
4. Search for `Jupyter` and click **Install** on the one made by Microsoft.

*(Alternative: If you already have Jupyter Notebook or JupyterLab installed via Anaconda, you can use that instead. But we recommend VS Code for this lab).*

---

## Step 3: Create Your Project Folder

Let's keep all your lab files in one place.

1. Create a new folder on your computer called `ML_Lab` (put it somewhere easy to find, like your Desktop or Documents).
2. Move the following files (provided by your instructor) into this `ML_Lab` folder:
   * `intro_ml_lab.ipynb` (The notebook you will be working in)
   * `requirements.txt` (The list of tools we need to install)

---

## Step 4: Create a Virtual Environment (`.venv`)

A virtual environment is an isolated "sandbox" for your project. It keeps the tools you install for this lab separate from the rest of your computer, preventing conflicts.

1. Open **VS Code**.
2. Go to **File > Open Folder** and select the `ML_Lab` folder you created.
3. Open the terminal inside VS Code by going to **Terminal > New Terminal** at the top menu.
4. In the terminal at the bottom of the screen, type the following command and press Enter:

   **For Windows:**
   ```bash
   python -m venv .venv
   ```
   **For Mac/Linux:**
   ```bash
   python3 -m venv .venv
   ```
   *(This creates a hidden folder called `.venv` inside your project).*

5. **Activate the virtual environment** by typing:

   **For Windows (Command Prompt):**
   ```bash
   .venv\Scripts\activate
   ```
   **For Mac/Linux (or Windows PowerShell):**
   ```bash
   source .venv/bin/activate
   ```
   *(You will know it worked if you see `(.venv)` at the beginning of your terminal prompt line).*

---

## Step 5: Install the Requirements

Now that your sandbox is active, let's install the tools we need for this lab (like scikit-learn, pandas, and matplotlib).

1. In the same VS Code terminal (make sure `(.venv)` is still showing), type:
   ```bash
   pip install -r requirements.txt
   ```
2. Press Enter and wait. You will see a lot of text scrolling by as it downloads and installs the libraries. This might take a minute or two.

---

## Step 6: Open and Run the Notebook!

You are fully set up. Now for the fun part.

1. In VS Code, look at the **Explorer** panel on the left side.
2. Double-click the file named `intro_ml_lab.ipynb` to open it.
3. **Select your Python Kernel:** 
   * In the top right corner of the notebook window, you will see a button that says **Select Kernel** (or it might already say `.venv`).
   * Click it, choose **Python Environments**, and then select the one that says `.venv (Python 3.x.x)`.
4. You are ready to go! 
   * To run a block of code (a "cell"), click inside it and press `Shift + Enter`.
   * Follow the instructions inside the notebook, read the comments, and complete the exercises at the end of each section.

---

## Troubleshooting Common Issues

* **"Python is not recognized as an internal or external command"** 
  * You likely missed the checkbox in Step 1. Uninstall Python, reinstall it, and make sure to check **"Add Python.exe to PATH"**.
* **VS Code says "Jupyter extension is required"**
  * Click the prompt that appears to install it, or go to the Extensions tab on the left and install the "Jupyter" extension manually.
* **I can't see the `.venv` folder in VS Code**
  * That's normal! Folders starting with a dot (`.`) are hidden by default on Mac/Linux. You don't need to click on it; just activate it through the terminal as shown in Step 4.