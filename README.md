# Python for data analysis

A set of notebooks to teach Python for data analysis in approx 24h.

## Notebooks

### Create the kernel

To run the notebooks, you have to create a kernel over the virtual environment.

You only need to do this once.

```
# Activate the virtual environment
pipenv shell

# Create the kernel
python -m ipykernel install --user --name='libropython'

# Exit the virtual environment shell
exit
```

### Run the notebooks

```
pipenv run jupyter notebook .
```
