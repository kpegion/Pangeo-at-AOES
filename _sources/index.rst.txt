.. Pangeo-at-AOES documentation master file, created by
   sphinx-quickstart on Sun Jan  5 21:07:44 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Pangeo-at-AOES
==========================================

.. image:: https://mybinder.org/badge_logo.svg
 :target: https://mybinder.org/v2/gh/kpegion/Pangeo-at-AOES/master

This is a set of Tutorials, including example Jupyter Notebooks, for using the Python and the Pangeo Software stack for data analysis on the AOES COLA Servers

This set of tutorials is specifically designed for the Mason AOES COLA Servers, datasets available on our servers, and use cases around common data analyses used by our students and faculty

Expectations Prior to these Tutorials
****************************************
1. You are a student or faculty in the GMU AOES Department
2. You have an account on the COLA servers.
3. You are familiar with basic Unix.  If you are not familiar with Unix, [Software Carpentry](https://software-carpentry.org/) provides a good basic [Unix Tutorial](http://swcarpentry.github.io/shell-novice/)
4. You have programming experience and a basic understandng of Python syntax. If you need to refresh your programming skills and/or learn Python syntax, [Software Carpentry](https://software-carpentry.org/) provides a [Programming with Python Tutorial](http://swcarpentry.github.io/python-novice-inflammation/)

.. toctree::
   :maxdepth: 1
   :caption: Getting Started

   setting-up-pangeo
   setting-up-jupyter


.. toctree::
   :maxdepth: 1
   :caption: Basic Reading and Plotting

   examples/read-netcdf.ipynb
   examples/read-grib.ipynb
   examples/read-opendap.ipynb

 
.. toctree::
   :maxdepth: 2
   :caption: Analysis Using Xarray
   :hidden:

   examples/advanced-analysis.ipynb


.. toctree::
   :maxdepth: 1
   :caption: Making Nice Plots

   examples/matplotlib-tutorial.ipynb
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
   :maxdepth: 3
   :caption: Python Packages

   scientific-python-packages
   what-is-pangeo
   other-useful-python-packages
