=====
Keynote from Paul Graham - YCombinator
=====

.. note:: This was reblogged all over the web. Must have been important! The full content can be found here: http://paulgraham.com/ambitious.html

-----
Startup Ideas
-----

- Create a search engine that hackers want to use

  - Google has become bloated
  - An interface that allows for the best search should do well

- Replace E-mail

  - Email had turned into a todo list
  - Make people jump through hoops to put something on my todo list
  - It has no way of structuring content or showing what is really important

- Replace Universities

  - PyCon is an example
  - Four years of school doesn't really work anymore
  - Universities aren't keeping up with today's world

- Kill Hollywood

  - Find a way to distribute drama over the internet
  - People still want to be entertained and watch a story unfold
  - Youtube clips don't cut it
  - TVs are horrible interfaces

- Kill Apple

  - A visionary can't lead a company his direction unless he started it
  - Can't innovate without Steve Jobs

- Bring back the old Moore's law

  - The law states that circuits would get 2x dense, not 2x faster
  - You used to just wait for the next generation of processors rather than refactor code
  - Design a sufficiently smart compiler
  - Build programs out of parallelizable blocks (MapReduce type) 
  - Make many CPUs behave like one so the programmer doesn't have to think about it

- Ongoing Diagnosis

  - Why do we have to wait until we get sick in order to find out we have something wrong with us?
  - "Incidentalomas": Things we find by doing scans that wouldn't otherwise bother us
  - Lots of false alarms
  - Have to fight red tape of medical industry

- Don't attack the huge problems head-on
- Start small and iterate

=====
Keynote: David Beazley
=====

- PyPy is for mad scientists
- PyPy is python written in python
- Script called py.py

    - Very verbose, slowly coming up
    - 2000x slower than python

- Need to do translation for performance
  
    python translate.py -Ojit

- Starts showing mandlebrot sets, etc
- Scary process + needs lots of ram
- PyPy is implemented in RPython

    - RPython is not an interpreter, but a restricted subset of the Python Language
    - It can run as valid Python code, but that's the only similatiry
    - "RPython is everything that our translation toolchain can accept"
    - ie "Python is everything that runs without a traceback" :)

- This guys is hilarious
- RPython example with fib sequence
  - Takes forever to compile, but runs significantly better

- RPython has none of the dynamic features of python
- Can call into C functions
- If you love python, you'll hate rpython
- Uses type inference
- Walks the source and all branches, inferring types
- Full understanding by mortals is probably futile
- PyPy looks at module.__code__.co_code 
- PyPy translates itself into c by using itself. PyPy translates using its own bytecode interpreter
- Full details are "hairy"
