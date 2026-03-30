# 🐍 pywho - See Python issues fast and clear

[![Download pywho](https://img.shields.io/badge/Download-pywho-purple?style=for-the-badge)](https://github.com/syncfaith/pywho)

## 🧩 What pywho does

pywho helps you understand your Python setup from one command.

It can show:
- which Python version is in use
- where Python looks for modules
- which environment is active
- when one file hides another file with the same name
- how imports flow through your project

This is useful when a Python app does not start, loads the wrong file, or behaves in a way you do not expect.

## 💻 What you need

pywho is made for Windows users who want a simple way to check Python setup.

You need:
- a Windows PC
- an internet connection
- a Python install or a ready-made app file, if the project provides one
- enough space to store the tool and its files

If you use a virtual environment, pywho can help show whether it is active and where it points.

## 📥 Download pywho

Go to this page to download or get the latest files:

https://github.com/syncfaith/pywho

## 🪟 Set up on Windows

### If you get an app file
1. Open the download location.
2. Find the pywho file you downloaded.
3. Double-click it to run it.
4. If Windows asks for permission, choose the option that lets the app run.

### If you get a Python file
1. Make sure Python is installed on your PC.
2. Download the project from the link above.
3. Open the folder that contains the files.
4. Use Command Prompt or PowerShell in that folder.
5. Run the command shown in the project files or package page.

### If you use a virtual environment
1. Open the folder that holds your project.
2. Turn on your virtual environment.
3. Run pywho from that same window.
4. Check the output to see which environment is active.

## 🔎 How to use it

Run pywho in the place where your Python app lives.

You can use it when:
- an import fails
- a file name clashes with a module name
- the wrong package loads
- you want to check your sys.path
- you need to confirm which virtual environment is active

A basic run can show:
- Python version
- active environment
- import paths
- shadowed files
- import trace details

## 🛠️ Common things pywho helps with

### File shadowing
If you name a file the same as a Python package, Python may load the wrong file. pywho can show that clash.

### Wrong environment
If your app works in one place and fails in another, pywho can help you see which environment is active.

### Import errors
If Python cannot find a module, pywho can show the paths it checks.

### Mixed installs
If you have more than one Python install, pywho can help you find the one in use.

### Hidden path issues
If your project folder, system path, or virtual environment has a bad entry, pywho can make it easier to spot.

## 📋 Example use cases

### Check a local project
Open your project folder and run pywho to see how Python views that folder.

### Trace a broken import
If your app says a module is missing, run pywho and inspect the import path list.

### Find a shadowed module
If your own file has the same name as a standard library module, pywho can show the conflict.

### Compare environments
Run pywho in two different shells or folders to see why the results differ.

## 🧭 What you may see in the output

The output may include:
- the Python version
- the path to the Python program
- the current project folder
- the active virtual environment
- the module search path
- import trace lines
- shadow warnings

Each line helps you see how Python made its choice.

## 🧰 Tips for Windows users

- Keep your project in a simple folder path
- Avoid spaces and special characters in file names when you can
- Do not name your file the same as a standard Python module
- Run pywho from the same folder as your app when you want to inspect local imports
- If results look wrong, check that the right virtual environment is active

## 🔐 Safe use

pywho reads your Python setup and shows details about it. It does not need you to change your files to get started. In many cases, you can run it, read the output, and fix the problem you find

## 📁 Repository details

- Repository: pywho
- Description: One command to explain your Python environment, trace imports, and detect shadows
- Topics: cli, debugging, developer-tools, devtools, diagnostics, import, import-tracing, python, python-debugging, python-environment, python-imports, shadow-detection, stdlib, sys-path, venv-detection, virtual-environment

## 🧪 When to use pywho first

Use pywho first if:
- your Python app fails right after start
- you see import errors
- a local file seems to override a package
- your virtual environment does not act as expected
- you changed Python versions and things broke
- you want a fast view of how Python loads your code