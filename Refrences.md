What is a refRence??
-----------------------------------------

```java
Box b1= new Box();
Box b2= b1;
b2.Height=20
b1.Height=10
```
What is the value of b2.Height?


Passby Value
-----------------------------------------
Pass by value is taking the data, and any changes made to that value will not be reflected in the original value

examples
-Primitives (int, double, float)

Pass by Refrence is when the **memory** memory adress to the actual parameter is passed to the method. 

**PASSING BY REFRENC IS NOT THE SAME AS PASSING AS REFRENCE**

-In java, a refrence is passed by value.

```java
public static void print(){
int a=1;
doubleN(a);
System.out.println(a); // what will this print?
}


public static voind doubleN(int a){
a=a*2;
}
```
a would still be 1 because it is a primitive

Privacy leaks
------------------------------------------------
- A privacy leak is when private data is being ascessed in places in where it shouldnt be acessed

privacy leaks help protect sensative data- and keep it from changes


