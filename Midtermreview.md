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
  
  
  

