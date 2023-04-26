Midterm Review
----------------------------------------------
YAY AY YAYA
I LOVE CODING!

Lets start

-Which of the following is TRUE regarding the array type in Java:

(A) length of the same array (e.g. int[]) cannot be modified
(B) can have mixed types such as int and float in one array
(C) allows fast data insertion and deletion comparing to a linked list
(D) allows O(1) random access to an element


- hmm An array is not chanagble at least in size- so the first one is correct.
- An array cannot have mixed types so B is incorrect
- Fast data inseration and deletion- no
- allows o(1) random access - I dont think so.

**A**

- Next problem
- Regarding the 'new' operator, which statement is TRUE?

(A) returns the memory location of a pre-existing object
(B) is always required when declaring a class-type variable
(C) must always be used when assigning values to variables
(D) creates (allocates) a new object in memory

- A is not correct as only if you print out the object, it returns the memory location
- B is not correct because it is not ALWAYS required
- C is also incorrect becaues it is not always used when assigning values to variables
- D is correct as everytime you use the "new" function, it creates a new object in memory


2pt) Dog and Cat classes both inherit the Animal class.

Assume the Animal class has a new function called dash():

public String dash();
And assume Cat and Dog classes have both overridden this function.

Now, suppose we want to keep 1000 Dog objects and 2000 Cat objects in the same array called animals, What should be the data type for this animals array so all elements of the array could call the dash() function in a loop?

(hint: Not the Object class)

**- The answer to this should be "Action" as the animal class implements the Action inheritence file. And as we saw earlier, we have code that already has an array with a smiliar goal.
```java
    Action[] animals= new Action[]{catone, dogone, snowball, curiousgeorge};

        for(Action freind: animals){
            freind.play(legotruck);
       }
```


 Write a function to check whether an int array is asymetrical.
 
 
 - this is easy, we start off with
```java
public static boolean isAsymetrical(int[] data) {
    if (data == null || data.length == 0 || data.length == 1) {
        return true;
    }
    int n = data.length;
    for (int i = 0; i < n / 2; i++) {
        if (data[i] != data[n - i - 1]) {
            return true;
        }
    }
    return false;
}
```



18. (5pt) Suppose 4 friends A, B, C and D are going across a bridge. Their time alone across the bridge is:

A: 1 min
B: 2 min
C: 10 min
D: 30 min
They have to follow the same rule as the "pets across bridge" problem discussed in lecture

Bridge can only allow up to two persons to pass at the same time
There's one lamp that must be used (held by one person) when crossing the bridge
(1pt) What's the shortest time for all 4 of them to cross the bridge?

(3pt) Explain the steps.


- Ok so for thsi problem we need to keep in track of some things. 

- The 2 longest should go together at some point but NOT in the first round

- so A and B can go together first and that takes 2 minutes

CD   -----------------------                time: 2 min ---------------------                   AB


then, A can go back- which takes another minute

CDA     ------------------------              time: 3 min      --------------------                B
-
Then, C and D go together - which takes 30 min

A      --------------------               time: 33 min  --------------------                BCD


Then, B can go back to A which takes 2 minutes

AB       ------------------               time 35 min      -------------------            CD


And AB can cross over which takes 2 min


  -------------------             time: 37 min  -------------------------               BCDA
                        
                        
                       
                       
  The shorteset time is 37 minitues
  
  
  
  
  
  ArrayList
  ----------------------------------
  -arrayLists are arrays that allow you to continue to add spaces to an array
  
  you can add to an arraylist
  
  Ex:
  
  Arraylist fruitList= new ArrayList();
  fruitList.add("mango");
   fruitList.add("apple");
    fruitList.add("bananna");
     fruitList.add("yes");
  
  
  Big O notation
  ------------------------------------
  
  Very epic!
  
  "How code slows as data grows"
  
  
  examples
  O(1)
  O(n)
  O(log n)
  O(n^2) 
  
  
  n= amount of data variable like x
  
  
Here is an exmaple

```java 
int addUp(int n){

int sum=0;
for(int i=0; i<=n; i++){

sum+=i;
}
return sum;
}
```

what if n=100000?
this function has an O(n) complexity
then n= would go for at least 10000 times because of the for loop

lets rewrite the code for clarity

 ```java
 int addUp(int n){
 int sum= n*(n+1)/2;
 return sum;
 }
 ```
 
 
 
 This will take only 3 steps
 even if n=100000
 
 this is an O(1) complexity cosntant time
 
 
 https://cdn-media-1.freecodecamp.org/images/uKzmoTrYJbLljumcgitSieybiHBUBEasqyvd
 
 Here is an example
 
 binary search is O(log n) - llogathmic time
 bubblesort is quadratic time
 
O(1)= constant time 
O(log n) - llogathmic time
O(n) is linear time
O(n log n)= quaslilier time
O(n^2)= quadratic time
O(n!)= factorial time


Returning the max number's index in an interger array
---------------------------------------

The input is an array of integers
so if you were given

```java
int [] data1= {12,12,1,7,18,10,3};

we need to return 4 because index 4 is 18
```



Object orientated Programming
-------------------------------------------------
Why Object oriented?

object orientated programming helps you read information


**Encapsulation**
Encapuslation is bascially using methods to set in classes

so 
```java
public class Student{

String name;
int age;
```
both of these will have 2 methods both set and get.

Bro basically just set and get what not


  
  
Overide vs Overload
----------------------------------------------- 


Here is a class Animal

```java
class Animal{
public void add(){

}

//another method with the same name but takes parameters

public void add (int a, int b){

}
```
- One of the methods have parameters unlike the other
- lets add another
```java
class Animal{
public void add(){

}

//another method with the same name but takes parameters

public void add (int a, int b){

}

public int add( int a, int b, int c){

}
```

-This is method overloading- as the names are the same, but have different parameters


the return type does not count in method overloading



Overiding
==========



```java
class Animal{
public void add(){

}

class Dog extends Animal{

}
```

the Dog class is the child class of animal- and it is the SAME animal class- it is a property of a dog class.

so whatever code is written in the add method, it becomes a property of the dog class. So if you want the same code from animal to dog, you need to add the same method so


```java
class Animal{
public void add(){

}

class Dog extends Animal{
public void add(){

}

}

both signatures of both add methods are COMPLETLY THE SAME.


Differences between overloading and overiding

Overloading

-Occurs in one class
-method has the same name, but different parameters
- increases readaibility- can use different names would still work 
-return type can be the same or different




Overrding 
-occurs in two classes: super clas and sub class ie: inheritance is involved

-Name and parameters both have to be the same.

- we use overiding to ensure that the method in the child class is already present in the parent class
- return typ ewill always be the same




Using protected
---------------------------------------------

WE can use "protected" in a base clas to make sre we can ascess the names in other classes.

- for a base function w never wnat to use, we have to make it and the whole class abstract. making an abstract class- make sit so we ust add other classes from the derived base class.


That means we cnannot initialize a new anima l!


- we can make an interface. Interfacees are a different version of inheritance. In the interface class, we can create an action method- an interface can have functions in it. Now that interface will call each play function in their respected classes. because dog is comnnected to animal and animal is connected to Action- their plays will make sense.

Now we can rewrite the array with Action instead!




-COol

Complexity (cost)

cost means your given code takes a certain amount of time, memory, space, power, cpu, network, and yes.
-------------------------------------------------

Different types of passses

one pass- each element used in constant times.
should not be a function of the size of the array
evey element should be used in the constant times.

Any sorts are not one pass!

Is binary search one pass?

How many times each element is looked at?

we start from the middle

So it can be UP to one pass so yes, it is!



