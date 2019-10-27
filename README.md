# Python for data analysis

A set of notebooks to teach Python for data analysis in approx 24h.

## Environment setup

### Requisites

Two options here:

* With Anaconda for Python 3 (recommended for basic users)
* With pipenv (recommended for advanced users), you will need:

  * Python 3.7
  * pipenv
  * jupyter

To install `pipenv` as a command, do:

```
sudo -H pip install -U pipenv
```

To install `jupyter` as a command, do:

```
sudo -H pip install -U jupyter
```

### Extra steps for pipenv users

#### Install the dependencies

You can skip this step if you're using Anaconda.

To install the dependencies (during the setup of the project, or in case other collaborator updates them):

```
# For development use
pipenv install --dev

# For production use
pipenv install
```

The first time you run it, it will create the virtual environment that contains all the project dependencies.

#### Create the notebooks kernel

You can skip this step if you're using Anaconda. When opening the notebooks, just select your anaconda kernel.

To run the notebooks if you're using a pipenv environment, you have to create a kernel over the virtual environment.

You only need to do this once.

```
# Activate the virtual environment
pipenv shell

# Create the kernel
python -m ipykernel install --user --name='libropython'

# Exit the virtual environment shell
exit
```

## Run the notebooks

```
pipenv run jupyter notebook .
```
