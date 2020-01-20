Setting up Pangeo & other Pytbon Packages  on the COLA Servers
################################################################

Now that we understand what Pangeo is and why we want to use it, let's talk about how to set it up and run it on the COLA servers.

Many of the examples provided in this tutorial will work using the COLA Anaconda Module, activated using ::
   module load anaconda/3

However, the COLA Anaconda Module may not have the latest version or may not include Python packages that you wish to use, especially non-standard packages such as `climpred` are not included.

I recommend installing your own version of miniconda (a mini version of Anaconda Python) which will allow you to install additional packages as you need without needing to ask Tom to install a package and so that you can develop custom testing environments in the future.  You may not see now why you would want this flexibility, but you will likely encounter the need down the road.  To do this I have reproduced the necessary steps from https://pangeo.io/setup_guides/hpc.html. 

1. Log into a COLA Server and from your home directory execute the following:

.. code-block:: bash

   wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
   chmod +x Miniconda3-latest-Linux-x86_64.sh
   ./Miniconda3-latest-Linux-x86_64.sh

2. The following command is necessary so that your new Python environment is not initiaized by default on login:

.. code-block:: bash

   conda config --set auto_activate_base false

3. Next, you want to make sure that your conda package manager is updated :

   .. code-block:: bash

   conda update conda


4. We will now create a conda (Python) environment with a specific set of packages installed:

.. code-block:: bash

   conda create -n aoes -c conda-forge \
       python=3.6 jupyterlab nbserverproxy \
       xarray scipy netcdf4 matplotlib cartopy dask \
       metpy climpred


You have now created a conda environment called pangeo. When you activiate this environment, you have access to Python 3.6 and all the packages listed here.  You may wonder, how do I know what packages to install?  No need to worry, you can install these for now and add others later if you realize you need them.

5. Now, let's activiate this environment so you can work in Python with these packages:

.. code-block:: bash

   conda activate aoes

