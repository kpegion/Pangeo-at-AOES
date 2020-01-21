Why Python?
###########################################

Why use Python instead of GrADS, ncl, Matlab?

1. Becoming very common in our field.
2. Has capabilities for handling Big Data.
3. Open Source: growing and adapting quickly; community can contribute

What is Pangeo?
###########################################

`Pangeo <https://pangeo.io/index.html>`_ describes itself as "A Community Platform for Big Data Geoscience".

I think of it as two things:

1. An evolving set of software and tools for data analysis in our field
2. An open and helpful community rich with useful information to advance my data analysis capabilities and research and share my knowledge to help others.

The Pangeo Software Stack
***************************
A loose collection of open source software consisting of Core Packages that are fundamental to Geoscience data anaylsis. They include: Xarray, Iris, Dask, and Jupyter.  

Xarray
-------
Website: http://xarray.pydata.org/en/stable/
Why is it useful? ::
Powerful tool for climate data analysis because it can perform operations on what they refer to as N-D labeled arrays and datasets.  What that means to us is that we can easily read in a netcdf or collection of netcdf (or grib) files and perform operations like calculating climatologies, means over specified dimensions, extracting regions, etc. while maintainng all the metadata and coordinate information with your data.  The ability to open many related netcdf files and perform operations over all the data in the files as if it was a single file is particularly useful.

Dask
-----
Website: https://dask.org/ 
Why is it useful? :: 
helps us to solve the problem of too much data to load into memory to accomplish our operations by provding "lazy loading of data" and parallelizing those operations.  This means you don't have to load all the data into memory to calculate that climatology AND you don't have to worry too much about how all that parallelization is done.  Xarray and Dask are integrated such that you can perform xarray operations in parallel with minimal effort on your part.  

Jupyter
---------
Website:  https://jupyter.org/
Why is it useful? ::
Provide a fabulous notebook environment which combines everything I ever dreamed of in data analysis.  My code, my data, my notes, my references, and my plots are all together in one place.  This makes it easy to write reproducible and sharable code.

Iris
-----
Website: (https://scitools.org.uk/iris/docs/latest/) 
Why is it useful?::
Seeks to provide a powerful, easy to use, and community-driven Python library for analysing and visualising meteorological and oceanographic data sets. This the one core package I am not familiar with.  AOES students or faculty who do work with Iris should feel free to update this documentation to provide more information.

