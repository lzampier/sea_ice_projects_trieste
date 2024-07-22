# Working with Conda for your project

## STEP ZERO – Installing conda

If you are lucky, `conda` is already installed in your system, either through Anaconda or Miniconda. Miniconda is a minimal installation of Anaconda, which will be enough for the scope of our project. Check if you have `conda` installed in your system by typing:

```
user@server:~$ conda
usage: conda [-h] [-v] [--no-plugins] [-V] COMMAND ...

conda is a tool for managing and deploying applications, environments and packages.

options:
 -h, --help          Show this help message and exit.
 -v, --verbose       Can be used multiple times. Once for detailed output, twice for INFO logging, thrice for DEBUG logging, four times for TRACE logging.
 --no-plugins        Disable all plugins that are not built into conda.
 -V, --version       Show the conda version number and exit.

commands:
 The following built-in and plugins subcommands are available.

etc...
```

If conda is not installed, and you are on a cluster or HPC system try `module load anaconda` or `module avail` to see if there is a conda installation available for you. If conda is still not installed, you can easily install miniconda on your platform of choice (Windows, Linux, Mac) by following [**this guide**](https://docs.anaconda.com/miniconda/). You might need to restart your shell after installing `conda`.

## STEP ONE – Create and activate a new environment

To create a new `conda` environment run:

```
conda create --name <my-env>
```

You should give a meaningful name to your environment (instead of `<my-env>`). The nice aspect of `conda` is that you can have multiple independent environments running in parallel on your machine. Once created, activate your environment by running.

```
conda activate <my-env>
```

## STEP TWO – Install mamba

`mamba` is a reimplementation of the conda package manager in C++. To make it simple, it runs faster than `conda` and I recommend installing and using it by running `conda install -c conda-forge mamba`.

## STEP THREE – Install the Python packages you need

Run the following commands, that should install everything you need for starting with your project.

```
mamba install -c conda-forge xarray dask netCDF4 bottleneck matplotlib cfgrib zarr dask gcsfs cmocean ipykernel scipy jupyterlab
```

The whole process is typically fast but can take up to a few minutes. The evolution of the installation can be monitored by a progress bar. Now you should be able to run `jupyter lab` from a shell with your active environment and find all the Python packages you installed already available there.
