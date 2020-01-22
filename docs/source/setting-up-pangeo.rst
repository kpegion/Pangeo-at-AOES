Setting up Pangeo & other Python Packages on the COLA Servers
################################################################

Now that we understand what Pangeo is and why we want to use it, let's talk about how to set it up and run it on the COLA servers.

1. Log into a COLA Server and from your home directory execute the following:

.. code-block:: bash

   git clone https://github.com/kpegion/Pangeo-at-AOES.git


2.  Go to the Pangeo-at-AOES directory:

.. code-block:: bash

   cd Pangeo-at-AOES

3. Load anaconda so that you have access to the `conda` command:

.. code-block:: bash

   module load anaconda/3

4. We will now create a conda (Python) environment with a specific set of packages installed:

.. code-block:: bash

   conda env create -f environment.yml

You have now created a conda environment called aoes. When you activiate this environment, you have access to Python 3.6 and all the packages listed here.  You may wonder, how do I know what packages to install?  No need to worry, all the packages you need for this tutorial have been installed.  If you want to install additional packages later, you can add them.

5. The following command is necessary so that your new Python environment is not initiaized by default on login:

.. code-block:: bash

   conda config --set auto_activate_base false


6. Now, let's activiate this environment so you can work in Python with these packages:

.. code-block:: bash

   conda activate aoes

