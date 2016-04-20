# r-jupyter-notebooks

## Summary
These notebooks are meant to serve as a basic introduction to using the R kernel within a jupyter notebook.  It assumes no knowledge of notebooks and some basic familiarity with the R language.

## Installing R into Jupyter

On Mac OSX, python 2.7 comes pre-installed.  A `conda` install was used to grab python 3 the R kernel.  [This](https://www.continuum.io/blog/developer/jupyter-and-conda-r) blog was used as a guide.

Essentially, python was already on the system (2.7) since it is a recent version of Mac OS X.  The following steps were used on this Mac OS X machine (Yosemite).  The install steps should be similar for Unix systems as well as recent versions Windows (however install directories will be different, etc.).

Change to `/Library/` directory.
Download Miniconda3 install script (flavor - OS X latest python 3, 64-bit) from [here](http://conda.pydata.org/miniconda.html)

Run Miniconda3 install script, for example:

> $ sudo ~/Documents/bin/scripts/Miniconda3-latest-MacOSX-x86_64.sh
Follow instructions and specified install to `/Library/miniconda3`

Now, download and install r-essentionals using `conda`.  This downloads and installs all necessary packages for using R in jupyter, as well as R itself (usually a very recent version, but might not be the latest) and popular R packages.  **WARNING:  This will install R and may become the default R so you may have to update your PATH or .bash_profile file to get back to the desired version.**  The install command is as follows:

> $ sudo conda install -c r r-essentials

Now, R and the essential packages are installed we still need to check that jupyter has the R kernel in its list.  This command will check:

> $ `jupyter kernelspec list`

If, `ir` or R is not listed, you may add it using R.  Open R and use this command:

> \> `IRkernel::installspec(user = TRUE)`

Now, recheck the kernel list for jupyter with:

> $ `jupyter kernelspec list`

Start a jupyter notebook as follows:

> $ `jupyter notebook`

Start a new notebook and ensure R is an option and that within the notebook R commands work.  You may want to check your package install path:

> $ > .libPath()

## License
Please see notebooks.  In general, MIT License.
