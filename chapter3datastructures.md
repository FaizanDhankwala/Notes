Linear Structures
-----------------------------
Linear structures can be thought of as having two ends. Sometimes these ends are referred to as
the “left” and the “right” or in some cases the “front” and the “rear.” You could also call them
the “top” and the “bottom.”
cool right?

What distinguishes one linear structure from another is the way in which items are added and removed, in particular
the location where these additions and removals occur. For example, a structure might allow
to be added at only one end. Some structures might allow items to be removed from
either end.

STacks
-------------------------------------------------
a stack is an ordered collection of items where the addition of new items and the removal of existing items always takes place at the same end
the base of the stack is significant because the items are stored in the stack are closer to the base.


Stacks occur in everyday situations. Almost any cafeteria has a stack of trays or plates. Of course you can only take one at the top.
Last In First out!
Here are some stack operations
```
Stack Operation Stack Contents Return Value
s.is_empty() [] True
s.push(4) [4]
s.push('dog') [4,'dog']
s.peek() [4,'dog'] 'dog'
s.push(True) [4,'dog',True]
s.size() [4,'dog',True] 3
s.is_empty() [4,'dog',True] False
s.push(8.4) [4,'dog',True,8.4]
s.pop() [4,'dog',True] 8.4
s.pop() [4,'dog'] True
s.size() [4,'dog'] 2
```


The Stack Abstract Data Type
it is defined by the foollowing structures and operations

- it is a collection of items where items are added to and reoved from the end called the "top"

• Stack() creates a new stack that is empty. It needs no parameters and returns an empty
stack.
• push(item) adds a new item to the top of the stack. It needs the item and returns
nothing.
• pop() removes the top item from the stack. It needs no parameters and returns the item.
The stack is modified.
• peek() returns the top item from the stack but does not remove it. It needs no parameters. The stack is not modified.
• is_empty() tests to see whether the stack is empty. It needs no parameters and returns
a boolean value.
• size() returns the number of items on the stack. It needs no parameters and returns an
integer.

COOL!

Now how do we implenet the stack in python.

We need a new class first.

Stacks are collection of elements so we need a collection of data, lets use a lsit. So we are using the list [2, 5, 3, 6, 7, 4]
WE only need to decide which end of the lsit will be considered the top of the stack and which one will be the base

once we make that decision, we can implenet the operations append and pop.

```
class Stack:
def __init__(self):
self.items = []
def is_empty(self):
return self.items == []
def push(self, item):
self.items.append(item)
def pop(self):
return self.items.pop()
def peek(self):
return self.items[len(self.items)-1]
def size(self):
return len(self.items)
```

As ytou can see we make a self list- that is empty-> []

then we set a function is_empty to return the items in self.

then we make a push function, which takes self- and introduces item

we take the tiems in self and add whatver items that are in "items" to that list

then the 
```
def pop(self):
return self.items.pop()
def peek(self):
return self.items[len(self.items)-1]
def size(self):
return len(self.items)
```
are just methods that allow different print outputs.


NOW! nothing will happen now, cause we didnt even make a stack. So lets make one

```
s = Stack()
print(s.is_empty())
s.push(4)
s.push('dog')
print(s.peek())
s.push(True)
print(s.size())
print(s.is_empty())
s.push(8.4)
print(s.pop())
print(s.pop())
print(s.size())
```

pushing allows us to add items
Once we use pop and append, the items will be moved permenantly unless you take them back
What each operation does:

```
Push: This operation is used to add an element to the top of the stack. It is also sometimes called "pushing onto the stack." When you push an element onto a stack, it becomes the new top element, and any existing elements remain below it.


So lets break it down
---------------------------------------------
[1]- this is website number one as an example
[1,2,3] now we are going to 3 websites
but we choose to go back on one website
so the computer will take out the first one- or the last one in the array
so we have
[1,2]
and we press the back button 2 more times so we get
[]
- thats the idea


so we are gonna do this in pyhton.

lets make a list- browsing_session=[]
now lets say the user goes to website number 1
then 2 then 3

browsing_session.append(1)
browsing_session.append(2)
browsing_session.append(3)
 [1,2,3]
now how do we remove the last item
its pop
so last= browsing_ession.pop()
print(browsing_session)
this will print [1,2]
browsing_session[-1]- this is the last item in the stack

print browsing_session[-1]
this is 2.

lets check if the wesbite is empty or not!

so if not browsing_essin
print("dissable")


