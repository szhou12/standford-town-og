# Table of Contents
- [Conda Virtual Environment](#conda-virtual-environment)
    - [Step 1: Create Conda Virtual Environment](#step-1-create-conda-virtual-environment)
    - [Step 2: Activate the Virtual Environment](#step-2-activate-the-virtual-environment)
    - [Step 3: Deactivate the Virtual Environment](#step-3-deactivate-the-virtual-environment)
- [Built-In Python Virtual Environment](#built-in-python-virtual-environment)
    - [Step 1: Create Python Virtual Environment](#step-1-create-python-virtual-environment)
    - [Step 2: Activate the Virtual Environment](#step-2-activate-the-virtual-environment)
    - [Step 3: Git Ignore](#step-3-git-ignore)
    - [Step 4: Deactivate the Virtual Environment](#step-4-deactivate-the-virtual-environment)
    - [Step 5: Delete the Virtual Environment](#step-5-delete-the-virtual-environment)
- [Manage Dependencies](#manage-dependencies)

# Conda Virtual Environment
Personal Note: I used Conda to create the virtual environment because it is easier for me to specify the Python version so that installing dependencies will not have any compatibility conflicts.
## Step 1: Create Conda Virtual Environment
```
cd to-this-project-directory

conda create --name standford-town python=3.9.12
```
## Step 2: Activate the Virtual Environment
```
conda activate standford-town
```
## Step 3: Deactivate the Virtual Environment
```
conda deactivate
```

# Built-In Python Virtual Environment
## Step 1: Create Python Virtual Environment
```
cd to-this-project-directory

# For macOS and Linux
python3 -m venv env
```
- `env` is the name of the virtual environment folder; you can name it anything you like. Name it as `env` is the standard practice. 
- You can name the virtual environments for all your Python projects `env` without conflicts because each virtual environment is isolated in its repective project directory.

## Step 2: Activate the Virtual Environment
Activation changes the PATH and shell commands to point to the Python binaries within `env`.
```
# For macOS and Linux
source env/bin/activate
```

## Step 3: Git Ignore
Add `env/` to `.gitignore` file.

## Step 4: Deactivate the Virtual Environment
Deactivate and revert to using the system’s default Python interpreter and settings.
```
deactivate
```

## Step 5: Delete the Virtual Environment
Make sure the virtual environment is deactivated before deleting it.
```
rm -rf env
```

# Manage Dependencies
**NOTE:** Installing/Managing any dependencies/packages needs to keep the virtual environment **activated**. 
- Install all dependencies from `requirements.txt`
```
pip install -r requirements.txt
```
- To keep track of your project’s dependencies by listing all installed packages and their versions into the `requirements.txt` file.
```
pip freeze > requirements.txt
```