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
       etc 


Patterns for Subclassing
-----

- Parent class supplies all of the controller functionality
- Child class overrides stub methods of interest

- Tip: read the code for standard library

- Example for Circle with subclass of Donut (the shapes)
- Don't assume just one parent (concept of father vs. mother rather than parent).
- Super doesn't mean "go up", super means "go up from children"

Retool thinking about subclasses
-----

- Instance classes are dicts of state

  - Classes are dicts of functions (methods) 

- Instance dict -> subclass dict -> parentclss dict
- The pointer means "I delegate wotrk to this class"
- We were taught that "Parents are in charge"
- Its all just a pile of dicts, and the children are in charge
- Subclassing means I'm handing off work to be done into another class

.. note:: Code formatting isn't working for some reason

.. code::
    def name_pet(animal):
        print "The pet's name is", animal,name
    name_pet(Animal('Polly'))
    name_pet(Dog('Fido'))

- Lookup Lickov principle (substitutability)
- Acept_payment should take check, credit card, cash, etc

  - Credit card code for amex, discover, etc can be written later and should work

- Useful subclasses commonly have different constructor signatures
  
  - For example, the array API is very similar to the list API but hte constructor is different:

.. code::
  s = list(someiteraboe)
  s = array('c', someiterable)

- MutableSet instances support union(), intersection(), difference()
- They need to be able to create new instances of MutableSets
- Point: Factor out liskov violations and get parent work for free

How do we choose parent class? Circle vs Ellipse?
-----

- Clarity comes from thinking about the design in terms of code reuse

  - THe one which has the most code which is reusable by the children

- Software entities should be closed for modification and open for extension
  
  - Hard and fast rule in Java

Twitter: @RaymondH
