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
4!-> 4 times 3 times 2 times 1=24
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


 The Fibonacci Sequence
 ---------------------------------
So the fibonacci sequence is a number sequence.
uhhh

1,1,2,3,5,8

So the previous 2 numbers will add up to the next one. It's simple really.

so what if we had a function called fib(n) that calculated this number sequence.

so if we had fib(3)-> we would have to return 2.

so whats the equation?

here it is

```
Fn=Fn-1 + Fn-2

```

As you can see, the (n-2) are *indexes* okay, so we are basically traveling back in the lineso we can grab those 2 numbers and add them

but the equation
```
Fn=Fn-1 + Fn-2

```

is somewhat bad as if what if you had F1 as F(n) then Fn-1 would be F(0) and F(-1)


So of course, we need a base case.

so here is the updated equation.

```

Fn={ F (n-1) + F(n-2)  IF n>=3
otherwise IF n==1 or n==2 --> return 1

```

This is the updated formula and it makes sense because we cant have anything below 3 as a base clase or else we would be getting into the zeroes.

ok so in code it would look like this


```
int fib(int n){
# we have to assume n is positive
if (n>=3) {return fib(n-1) + fib(n-2);}
else {return 1;}
```


Lets see this function in action

lets take 4 as the argument

4 is greater than 3 so
fib(4)= fib(3) + fib(2).

 fib(2) is not greater than 3 so it returns 1
now fib(3)==3 so it reutrns fib(2) + fib(1)

so we know fib(2) and we know fib(1)= both equal 1

fib(3)= 1 + 1
so fib(3)=2.

and now we can calucate fib(4) because we have all the values


fib(4)= 2 + 1= 3.

and that is the correct answer.














