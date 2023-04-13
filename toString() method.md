toString() METHOD
-------------------------------


-This note will be about toString() methods

-The toString() method basically helps you print out an object.

Like a whole class instead of having multiple print statements blah blah

lets start
----------------------------------------------------------------------------

- we have two files

```java
public class Dragon{

}
```
and

```java
public class toStringmain{
public static void main(String[] args){

}
}
```

- we have the file and its driver (the main).

Again what do we need? We need to put some stuff into the Dragon file. Lets start with color, height, and what fire it breathes

```java
public class Dragon{
private String color;
private double height;
private String typeofFire;

}
```
- We need getters and setters now.

```java
public class Dragon {
private String color;
private double height;

private String typeOfFire;

// we need getters and setters

    public void setColor(String color){
        this.color=color;
    }
    public String getColor(){
        return color;
    }
    public void setHeight(double height){
        this.height=height;
    }
    public double getHeight(){
        return height;
    }
    public void setTypeOfFire(String typeOfFire){
        this.typeOfFire=typeOfFire;
    }
    public String getTypeOfFire(){
        return typeOfFire;
    }
 ```
    
  Next Step
   ----------------------------------------------------------------
   - we need to create a dragon in the main method. Lets do that real quick.
   This dragon will have
   
   -red scales
   
   - will be 180 meters tall
   - 
   - and will breathe helium
   - 
   - well call him DAONE


```java
    public static void main(String[] args){

        Dragon DAONE= new Dragon();

        DAONE.setColor("red");
        DAONE.setHeight(180);
        DAONE.setTypeOfFire("helium");

        
    }
}
```

-Ok so that is our code so far. DAONE is a cool red dragon that has all of that. Lets print it out using just the object and not the get functions!


```java
    public static void main(String[] args){

        Dragon DAONE= new Dragon();

        DAONE.setColor("red");
        DAONE.setHeight(180);
        DAONE.setTypeOfFire("helium");

        **System.out.println(DAONE);**
    }
}
```

we get this as the output 
```java
Dragon@7b23ec81
```

-This is because this is the objects place in the memory itself so it cannot actually print out everything until you tell it to.

Implmenting the toString() method
--------------------------------------------------

- Lets go back into the Dragon class
- and now we have to create a method that **MUST** have "toString()" as its name.

```java
public String toString(){

}
```

-in this method, we can give it basically a prompt to return.
Lets create a sentence that describes a certain dragon 

```java
 public String toString(){
         return "this dragon's color is " + color + " and it is " + height + " meters tall. Careful!, it breathes " + typeOfFire + "!";

    }
```
- now if we run the main class, we get
**this dragon's color is red and it is 180.0 meters tall. Careful!, it breathes helium!**

What is happening here?
- we are essentially replacing the object with a String- using the variables as placeholders
------------------------------------------------------------------------------------------------------------------

**FULL CODES**

**DRAGON CODE**
```java
public class Dragon {
private String color;
private double height;

private String typeOfFire;

// we need getters and setters

    public void setColor(String color){
        this.color=color;
    }
    public String getColor(){
        return color;
    }
    public void setHeight(double height){
        this.height=height;
    }
    public double getHeight(){
        return height;
    }
    public void setTypeOfFire(String typeOfFire){
        this.typeOfFire=typeOfFire;
    }
    public String getTypeOfFire(){
        return typeOfFire;
    }
    // we have the setters and getters now.

    // lets do the toString method here
    // we need it to be public

    public String toString(){
        return "this dragon's color is " + color + " and it is " + height + " meters tall. Careful!, it breathes " + typeOfFire + "!";


    }

}
```

**DRAGON MAIN CODE (TOSTRINGMAIN)**

```java
public class ToStringmain {
    //the toString method basically helps you print an object
    //lets add a main

    public static void main(String[] args){

        Dragon DAONE= new Dragon();

        DAONE.setColor("red");
        DAONE.setHeight(180);
        DAONE.setTypeOfFire("helium");

        System.out.println(DAONE);


    }
}
```
END OF NOTE



   
