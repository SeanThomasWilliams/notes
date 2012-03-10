=====
Python and Apache Caddandra
=====

- Logo looks like a female's eye
- Slides available at http://goo.gl/8Byd8
- Cassandra is an ordered document database.
- Select a column type, from there, select a key. Now you get all available values for that key.

- Example::    

    UserInfo:
      John:
        OrderedDict( age:32,
                     sex:'m'
                     etc...)

- Get the RPM packages from DataStax
- Has Thrift interface: Don't use it!
- Use pycassa: Provides simple access to Cassandra
- Cassandra allows for MapReduce
- Excellent for time series data. Allows for key associated with time / uuid.
- You can specify the data type for a column
- Pycassa allows for python object storage::

    self.name = "Sean"
    self.sage = "27"
    pycassa.put(self)

- Allows for primary and some secondary indexes

