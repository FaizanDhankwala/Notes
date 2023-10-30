-Each class should have a __Str__ method- this gives it a meanigful string represnetation
-Each class should also have a __repr__ method for representation in the shell.
-Each class shpuld be comparable so it can be sorted and compared with other instances. Thos means at least you should implement __eq__ and __lt__
you can find how many thigns the container holds using len

Lets start off with some basic code
--------------------------------------------------------
```
import random

class MSDie:
    """
    Multi-sided die

    Instance Variables:
        current_value
        num_sides

    """

    def __init__(self, num_sides):
        self.num_sides = num_sides
        self.current_value = self.roll()

    def roll(self):
        self.current_value = random.randrange(1,self.num_sides+1)
        return self.current_value

my_die = MSDie(6)
for i in range(5):
    print(my_die, my_die.current_value)
    my_die.roll()

d_list = [MSDie(6), MSDie(20)]
print(d_list)
```




