.. Pangeo-at-AOES documentation master file, created by
   sphinx-quickstart on Sun Jan  5 21:07:44 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Pangeo at AOES
==========================================

This is a collection of information and example Jupyter Notebooks, for using the Python and the Pangeo Software stack for data analysis on the Mason AOES/COLA Servers

This set of exampless is specifically designed for the Mason AOES/COLA Servers, datasets available on our servers, and use cases around common data analyses used by our students and faculty.


The examples are generally relevant to for basic climate data analysis.  Therefore, an external-tutorial_ is also provided for those without access to the Mason AOES/COLA Servers.


.. toctree::
   :maxdepth: 1
   :caption: Prerequisites

   prereq.rst


.. toctree::
   :maxdepth: 1
   :caption: Getting Started

   why-python-and-pangeo
   setting-up-pangeo
   setting-up-jupyter


.. toctree::
   :maxdepth: 1
   :caption: Reading Data

   examples/read-netcdf.ipynb
   examples/read-grib.ipynb
   examples/read-opendap.ipynb

 
.. toctree::
   :maxdepth: s12
   :caption: Climate Data using Xarray

   about-xarray
   examples/advanced-analysis.ipynb


.. toctree::
   :maxdepth: 1
   :caption: Plotting using Matplotlib 

   about-matplotlib
   examples/matplotlib-tutorial.ipynb


.. toctree::
   :maxdepth: 1
   :caption: Maps using Cartopy

   about-cartopy
   examples/cartopy-tutorial.ipynb


.. toctree::
   :maxdepth: 1
   :caption: Hindcasts with climpred

   about-climpred.rst
   examples/monthly-enso-subx-example.ipynb
   examples/daily-subx-example.ipynb


.. toctree::
   :maxdepth: 1
   :caption: Weather Data with Metpy

   metpy-tutorial.rst
   examples/metpy-constants-and-units.ipynb
   examples/metpy-calc.ipynb
   examples/metpy-plot.ipynb
   examples/metpy-sounding-dignostic.ipynb


.. toctree::
   :maxdepth: 1
   :caption: External Tutorial

   external.rst
