# Setting a Python developent environmet on macOS

## Step 1: installing command line tools

Open a terminal window and run the folloing line:

```terminal
xcode-select --install
```

## Step 2: Install VSCode

1. Install VSCode from internet
2. Install the following extension in VSCode
    - Python
    - Jupyter
- Note: both installations will install more dependecies

## Step 3: Installing hombrew
(this is similar to apt in linux)
Here is the source: https://brew.sh

Open a terminal and run the following line:

```terminal
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

## Step 4: Installing PyEnv

1. On a new terminal, run:

```terminal
brew update
```

2. Install pyenv running:
```terminal
brew install pyenv
```

## Step 5: Setting up PyEnv

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

## Step 6: Installing venv for pyenv

Run on a terminal:

```terminal
brew install pyenv-virtualenv
```
Finally restart your computer.

## Testing
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
