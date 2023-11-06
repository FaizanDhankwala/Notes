CAlculating time complexity with Recursion
--------------------------------------------------------------

Sum(n)=n+ sum(n-1)
sum(n)=n+sum(n-1)
fac(n)=n*fac(n-1)

TOH(n,A,B,C)

Fibbonaci- REcursive
Findig time complexity.


Recursion is when a function calls itself.

An example.


The thing about recursions is that there are 2 examples. The first example has to do with factorials.

Let me explain
----------------------------

A factorial is when a number is constantly multiplied by itself.

For example.
4!-> 4*3*2*1=24
You see?
so in essence it is 

```
n!=n*(n-1)*(n-2) --- 3*2*1
```

As the number is n=
and each time the number will decrease each time so it goes down each time.
But if you really think about it
take 4! for example,

4!-> 4*3*2*1 right?
but dosent that just mean it is 
4!->4*3*2!?
or 4!->4*3!?

so in theory the new equation would be
n! (any number factorial) is n*(n-1)!
"Any number factorial is that number times that number-1's factorail"

The only problem with this is 0-> as 0-1 -1 and that dosent work.

This is where we introduce

The Base Case
------------------------------

Because we need a case that has to equal one or stop in some way we can rewrite the equation to

```
n!={n*(n-1)!    IF  n>=1
otherwaise return 1
```

as you can see, the equation above has restriction so the value of n cannot be less than 1

Lets break down the process.


Lets do f(4)!

ok so 4 is greater than 1

so f(4) will be 4*3!

now we have 3!

lets plug it back in

so f(3)= 3*2!
because 3 >=1

now we have 2!

lets plug it back in
2>=1 so

f(2)=2*1!

now we have 1!
1=1

so f(1)= 1*0!

0! is not greater or equal to 1

so we return 1

*so f(1)=1*

no we know 1 factorial, we can plug it back in for f(2)

so f(2)= 2*1=2

*so f(2)=2*

now we can plug that back in into f(3)

 f(3)=3*2=6

 *f(3)=6*

 lets plug that last one into the original equaition

 f(4)=4*6 (because f(3)=6)

 *so f(4)=24*

 aaaand done!!!

 








