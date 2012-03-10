=====
Timeseries in Python
=====

Options:
- Numpy Arrays
- Scikit.timeseries
- Pandas

Numpy Arrays:
- Hard to pass around labels
- Memory mapped file::
  
    numpy import memmap
    image = memmap('some_file.dat',
    dtype=uint16,
    mode='r+',
    shape=(5,5),
    offset=header_size)

    from numpy import memmap
    a = memmap('some_file.dat', dtype=uint8,
                mode=write, ...)

Pandas
- Offers thing wrappers around 1,2,3D Numpy arrays.
- http://pandas.sourceforge.net
- Offers:
  - Axis labeling
  - Data alignment
    management of missing data
    many statistical tools
    easy visualization (line, var chart, boxplit) with matplotlib

::

    from pandas import *
    a = [12.3, 1,3,4, np.nan, 43
    ts = Series(a, index=DateRqange('1/1/2000', periods = 6, offset = datetools.day), name =...

- Nice readable output
- Data alignment, reduction, missing value management

::

    ts.align(ts2)
    ts.reindex(ts2.index)
    ts.groupby().apply()
    ts.fillna(0.0)
    ts.dropns()
    ts.to_sparse()

- He directs us to his github (Name is Johnathan Rocher) - https://github.com/jonathanrocher  
- This shows how to downsample, filter, reorganize

Storing your data?
-----

- txt, csv
- binary (watch out!)
- json: json
- HDF: pytables, h5py, pyhdf
- netCDF: netCDF4 (also scipy.io.netcdf)

Databases:
- SQL: sqlalchemy....

- HDF5 is the best way to store large datasets during/after processing
  - Formats are self-describing
  - Using pytables (fast, efficient)
  - Comparison if H5py vs Pytables
  - Compression (blosc9, h5py gzip, h5py lzo)

Can compute using out of core calculations with tables.Expr(blosc)
  - Very fast

Visualization
- s.describe() :: count, mean, std, min, max, etc
- correlation, covariance
- ts.plot()
  df.boxplot()

Chaco = Vis tool + vis toolkit for building custom graphical tools

