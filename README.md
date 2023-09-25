# Setting a Python developent environmet on macOS

This instructions will guide you to properly install PyEnv and PyEnv-VirtualEnv on macOS. PyEnv allows you to install and switch between multiple versions of Python. Combined with VirtualEnv you can manage Python environments from any of you installed Python versions. Then you can set any of your Python versions and enviroments easily and access them direclty (e.g., using Visual Studio Code).

This tutorial has four sections:
- Preparing the environment
- Installing PyEnv
- Installing PyEnv-VirtualEnv
- Testing the installation and getting used
  
## Section 1: Preparing the environment

### 1. Installing command line tools
This is a tool, developed by Apple, which install all the requierements and developer tools on mac. To install it, just open a new terminal window and run:
```terminal
xcode-select --install
```
The a window pop-up to confirm the installation. It will take time to finish depending on your internet connection.

### 2. Installing Visual Studio Code (VSCode)
Visual Studio Code is a powerful code editor. I strongly suggest to use it, but you can omit this step if you want to use another one. Just enter to [VSCode Download link](https://code.visualstudio.com/download) and follow the installation.

### 3. Installing Python packages on VSCode
Click on packages in the left side of VSCode and look for the following packages:
    - Python
    - Jupyter
- Note: both installations will install more dependecies

### 4. Installing Homebrew
Homebrew is the easiest and most flexible way to install the UNIX tools Apple didn’t include with macOS. You can check the installation directly on [Homebrew webpage](https://brew.sh) or just run the following line on terminal.
```terminal
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Section 2: Installing PyEnv

### 1. Install PyEnv using brew
Now we will use the recently installed homebrew, which comes with the brew command. In this case just run the following two commands one by one.
```terminal
brew update
```
```terminal
brew install pyenv
```
### 2. Setting up PyEnv
Run the following commands one by one:
```terminal
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
```
```terminal
echo 'command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
```
```terminal
echo 'eval "$(pyenv init -)"' >> ~/.zshrc
```
```terminal
brew install xz
``````

## Section 3: Installing PyEnv-VirtualEnv

Run on a terminal:

```terminal
brew install pyenv-virtualenv
```
Finally restart your computer.


## Section 4: Testing the installation and getting used
(I need to check if you will need an extra step)

### Installing a python version:

The following line will be installing Python3.11.5

```terminal
pyenv install 3.11.5
```

### Setting up an environment

The following line will create a test env using 3.11.5

```terminal
pyenv virtualenv 3.11.5 test
```

### Opening a python env on terminal:

```terminal
pyenv shell test
```
```terminal
pyenv versions
```

Can you send me an screenshot here (of your terminal)
