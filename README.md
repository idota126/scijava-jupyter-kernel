# scijava-jupyter-kernel
[![Travis branch](https://img.shields.io/travis/hadim/scijava-jupyter-kernel/master.svg?style=flat-square)](https://travis-ci.org/hadim/scijava-jupyter-kernel)
[![License](https://img.shields.io/github/license/hadim/scijava-jupyter-kernel.svg?style=flat-square)](https://github.com/hadim/scijava-jupyter-kernel/blob/master/LICENSE)
[![Anaconda-Server Badge](https://anaconda.org/conda-forge/scijava-jupyter-kernel/badges/version.svg)](https://anaconda.org/conda-forge/scijava-jupyter-kernel)
[![Anaconda-Server Badge](https://anaconda.org/conda-forge/scijava-jupyter-kernel/badges/downloads.svg)](https://anaconda.org/conda-forge/scijava-jupyter-kernel)

---

`scijava-jupyter-kernel` aims to be a [Jupyter](http://jupyter.org/) kernel that integrate well with [ImageJ](http://imagej.net). See [here](https://imagej.net/Scijava_Jupyter_Kernel) for more details.

*Under the hood `scijava-jupyter-kernel` uses the [Beaker base kernel](https://github.com/twosigma/beakerx/tree/master/kernel/base).*

[Scripting languages](https://imagej.net/Scripting#Supported_languages) supported are :

- Groovy
- Python
- BeanShell
- Clojure
- Java
- JavaScript
- R
- Ruby
- Scala

## Documentation

A documentation in the forms of a serie of notebooks is available [here](./notebooks/Welcome.ipynb).

## Installation - Standalone

- Install [Anaconda](https://www.continuum.io/downloads)
- Install `scijava-jupyter-kernel` with :

```bash
# Add the conda-forge channel
conda config --add channels conda-forge

# Create an isolated environment called `java_env` and install the kernel
conda create --name java_env scijava-jupyter-kernel
```

- Usage :

```bash
# Activate the `java_env` environment
source install java_env

# Check the kernels have been installed
jupyter kernelspec list

# Launch your favorite Jupyter client
jupyter notebook

# or
jupyter lab
```

*Note : It is suggested to install the kernel in an isolated Conda environment (not in the root environment).*

## Installation - With Fiji integration

- [Download the last released JAR file](https://github.com/hadim/scijava-jupyter-kernel/releases).
- Drop it in your Fiji plugins directory.
- Start Fiji and launch `Analyze > Jupyter Kernel > Install Scijava Kernel`.
- Set the path to your Python binary.
- Choose a language (for example `jython` or `groovy`) or you can choose to install all the available languages.
- Choose a log level.

- Check the kernels have been installed with : `jupyter kernelspec list`.
- Launch `jupyter notebook` or `jupyter lab` and **select the kernel you want in the kernel list**.

![Scijava Jupyter Kernel Installation](teaser.gif)

## Development

- [CI with Travis](https://travis-ci.org/hadim/scijava-jupyter-kernel) makes sure the project builds without errors for each new commit.
- All the [notebook examples](./notebooks) are executed by the kernel during CI with [nbconvert](http://nbconvert.readthedocs.io/en/latest/execute_api.html).
- A [Conda package](https://github.com/conda-forge/scijava-jupyter-kernel-feedstock) is built for each new release.

## License

Under Apache 2.0 license. See [LICENSE](LICENSE).

## Authors

- Hadrien Mary <hadrien.mary@gmail.com>
