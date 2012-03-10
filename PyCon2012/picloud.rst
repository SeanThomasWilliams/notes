=====
The Journey to Give Every Scientist a Supercomputer
=====

- Computing power as a utility!
- You have a supercomputer at your fingertips.

::
    def sq(x):
        print "hello world"
        return x*x

    import cloud
    j = cloud.call(sq, 9)

    j # job id
    cloud.status(j)
    >>> 'done'
    cloud.result(j)
    >>> 81

    cloud.info(j)
    >>> exception: None, runtime, datatus, stderr, stdout....

    js = cloud.map(sq, range(20))

    js
    cloud.result(js)
    [0...361]

    js = cloud.map(sq, range(20), _type="c2") # C2 is a faster machine
    cloud.status(js)
    >>> ['done', 'done'....]

- Objects as arguments
  - Anonymous functions
- Calling non-python programs from python
- Environments are created and saved so you can call out to binaries, special modules, etc
- He goes on to tell us how great he is and that he graduated from Berkeley 
- Talks about how PyCloud came about - Face tagger in python
