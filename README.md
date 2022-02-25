# Notebook implementation
##### ***Source**: Python 3 Object-oriented Programming Second Edition , Dusty Phillips, 2018*
### Imports
```
from notebook import Notebook
from menu import Menu
```
### Running the program
```
Menu().run()
```
##### Notebook Menu
1. Show all Notes
2. Search Notes
3. Add Note
4. Modify Note
5. Quit
### Creating new notebook
```
>>> notebook = Notebook()
>>> notebook.new_note("Note 1")
>>> notebook.new_note("Note 2")
>>> notebook.notes
[<note.Note object at 0x107edd280>, <note.Note object at 0x107edd310>]
```
### Self
self represents the instance of the class. By using the “self” keyword we can access the attributes and methods of the class in python. It binds the attributes with the given arguments.
```
notebook1 = Notebook()
Notebook.new_note(self=notebook1)
```
### Built-in Methods
```
>>> dir(Notebook)
['__class__', 
'__delattr__', 
'__dict__', 
'__dir__', 
'__doc__', 
'__eq__', 
'__format__', 
'__ge__', 
'__getattribute__', 
'__gt__', 
'__hash__', 
'__init__', 
'__init_subclass__', 
'__le__', 
'__lt__', 
'__module__', 
'__ne__', 
'__new__', 
'__reduce__', 
'__reduce_ex__', 
'__repr__', 
'__setattr__', 
'__sizeof__', 
'__str__', 
'__subclasshook__', 
'__weakref__', 
'_find_note', 
'modify_memo', 
'modify_tags', 
'new_note', 
'search']
```
### Class attributes
Class attributes are attributes which are owned by the class itself. 
They will be shared by all the instances of the class.
##### Notebook
```
>>> notebook = Notebook()
>>> notebook.new_note("Heey, Jude!")
>>> notebook.new_note("Help! I need somebody!")
>>> for attr, val in notebook.__dict__.items():
...   print(attr, '-->', val)
notes --> [<note.Note object at 0x1086b0e20>, <note.Note object at 0x1086b0eb0>]
```
##### Note
```
>>> for attr, val in notebook.notes[0].__dict__.items():
...     print(attr, '-->', val)
memo --> Heey, Jude!
tags --> 
creation_date --> 2022-02-25
id --> 1
```
