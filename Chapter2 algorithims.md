-Big O notation
------------------------------------
helpful to count assignment statements. (The_sum=0)
big O notation is order of magnitude. 
also can be written as O(f(n))
as n gets large, the constant 1 will become less and less signifacnt to the final result

Here are all the functions of n
```
1 Constant
log 𝑛 Logarithmic
𝑛 Linear
𝑛 log 𝑛 Log Linear
𝑛
2 Quadratic
𝑛
3 Cubic
2
𝑛 Exponential
```

so for a function that asks for the sum of all the values in a array
How much time does it take to run this function?
this question is too  complex because your computer depends on it

How does the runtime of this function grow?

there are different times of time complexity

linear time- time increases linear.
constant time- does nto increase time as size of the function increases. The graph looks straight
quadratic time- when the time it takes to complete function increases like a quadratic functio 

Big O notation can take the place of these worlds

Linear- O(n) n represents the number of elements in the array
Constant-  O(1)
Quadratic- O(n^2)

how to find out which is which

-ASk yourself which is the fastest growing term.
- take out the coefficient.

  so T=an+ b

  so b obviously dosent grow that fast but a is multiplied by n so it will grow a lot faster
  - take out the coefficient so take out a.
  - you are left with n- so your time complexity is O(n).
 
    example 2.
    what if it is T=cn^2 +dn + e
    c, d, and e are constants

    - fund the fastest growing. Obivusly in this case is cn^2 as it is squared
    - take out the coefficient. so take out c.
    - you are left with n^2
    - so your time complexity is O(n^2)
   
      What about T=c=0.115

      we only have 0.115 so its already the fastest growing
      the only coefficent is the whole thing
      so we have to take out 0.115
      and so the time complexity is O(1)
      as the time is constant. THE WHOLE THING IS A CONSTANT!
      O(1) is better than O(n)


      Is their a faster way to find the time complexity without doin aalat?

      yes

      If you add 2 constant times, you still get O(1)

      def find_sum(given_Array)
      total=0--> this take s o O(1)
      for each i in given_Array: ---> Also takes O(1)
      total+=i --> this takes also O(1)
      return total --> this also takes O(1)

      This way we cna find the sum of all the numbers in the given_Array.


      Lets fimd the total time

      T_2 = O(1) + n* O(1) + O(1) --? the n is there to represent the for loop!
      If you add all these you get
      c_4 + n * c5.

      but! this time if we take outt the coefficient, we get n! soo the time complexity is O(n)

Example 4
----------------------------------------------------------
    
  array_2d= this is a 2 dimensional array

= [[1,4,3],
  [3,1,9],
  [0,5,2]]

  ok
  total=0
  so we are gonna run a NESTED loop already its like n^2

  for each row in array_2d
  for each i in row:
  total +=i-> O(1)
  return total: -> O(1)

  So the result is T_3= O(1) + n^2 (from the nested loop *O(1) + O(1)

  so the time complexity is O(n^2) as we isolate the fastest growing coeffient!


  Here are the time complexities of othe roperations!
  -------------------------------------

  ```
Operation Big-O Efficiency
indexx[] 𝑂(1)
index assignment 𝑂(1)
append 𝑂(1)
pop() 𝑂(1)
pop(i) 𝑂(𝑛)
insert(i,item) 𝑂(𝑛)
del operator 𝑂(𝑛)
iteration 𝑂(𝑛)
contains (in) 𝑂(𝑛)
get slice [x:y] 𝑂(𝑘)
del slice 𝑂(𝑛)
set slice 𝑂(𝑛 + 𝑘)
reverse 𝑂(𝑛)
concatenate 𝑂(𝑘)
sort 𝑂(𝑛 log 𝑛)
multiply 𝑂(𝑛𝑘)

```

And here is the complexities of dictionaries
----------------------------

```
Operation Big-O Efficiency
copy 𝑂(𝑛)
get item 𝑂(1)
set item 𝑂(1)
delete item 𝑂(1)
contains (in) 𝑂(1)
iteration 𝑂(𝑛)
```


  

  

      
