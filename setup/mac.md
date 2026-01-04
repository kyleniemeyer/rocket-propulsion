# Mac environment setup

## Installing Python

For detailed instructions and multiple options, see the official Python 
[documentation for installing Python on macOS](https://docs.python.org/3/using/mac.html).

However, I recommend choosing one of two routes:
1. Install Python and set up your environment via the command line
2. Install Anaconda distribution for a GUI-based approach.

### Command line installation route

:::{tip}
This is my preferred way to install Python and set up your computing environment.
:::

1. First, install [Homebrew](https://brew.sh), if you don't already have it 

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Anaconda installation route

If you prefer, you can install the [Anaconda distribution](https://www.anaconda.com/download),
which simultaneously installs Python, a large number of popular scientific modules, 
and a package/environment manager.

For students, make sure you register using your university email address for free access.
Anaconda is a commercial product, and has strict licensing and pricing for non-educational uses.

Anaconda provides detailed [installation instructions](https://www.anaconda.com/docs/getting-started/anaconda/install#basic-install-instructions).

## Setting up computing environment


Although Python is quite powerful out of the box, a massive ecosystem of third-party packages greatly extends its usefulness, particularly when handling scientific and engineering problems. To use these, you'll either need to install them into your Python environment via the shell (on Mac or Linux), or install using [Anaconda](https://www.anaconda.com/download).

On a Mac or Linux machine, I recommend using the built-in [`venv` module](https://docs.python.org/3/library/venv.html) to create a virtual environment for your work, then install inside that using the `pip` installer. Virtual environments are lightweight installations of packages in a particular location (such as in your working directory/project folder) that build on top of your system Python installation.

First, make sure you have a recent version of Python installed; I recommend 3.13.x, to avoid compatibility issues with the latest version of Python and some packages.

On Macs, use [`homebrew`](https://brew.sh): `brew install python@3.13`.

On a Linux variant, use the appropriate package manager. For example, on Ubuntu:
```bash
sudo apt-get update
sudo apt-get install python3.13
```

Then, in your project folder, create and activate the virtual environment: 
```bash
python3 -m venv .venv
source .venv/bin/activate
```

(Depending on your shell configuration, you might see `.(venv)` next to the path to indicate the active virtual environment.)

Now, you can safely use `pip` to install the necessary packages: 
```bash
pip install numpy scipy matplotlib pint fluids cantera
```

If you start a new terminal session, all you need to do is enter `source .venv/bin/activate` to reactivate the environment.