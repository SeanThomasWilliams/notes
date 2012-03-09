=====
The Art of Subclassing
=====

- Going to talk about classes and subclasses, what it means to be a class, etc
- Use cases, how super() works
- Examples from sandard library

class Animal:
  'Generic animal class'

  def __init__(self, name):
    self.name = name

  def walk(self):
    print('{} is walking'.format(name))

class Dog(Animal):
...etc


