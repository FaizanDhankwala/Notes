Getters And Setters
---------------------------------------------------

- These notes will be about getters and setters as well as how to use them

- for this program we will be coding a file called "cat"

lets start. we will have two class, a cat class and a main class.

-----------------------------------------------------------------
**THE CAT CLASS**
```java
public class cat{

}
```
** THE MAIN CLASS **
```java
public static void main(String[] args){

}
```
-So now we need to add instance variables in the cat class. These should be **Private**

```java
public class cat{
private int age;
private String color;
private String sound;

//this is some of the things all cats have

}
```
- now we will start with setters
```java
public void setage(int age){
this.age=age;
}
```
the first age is the age in the method- and the second age is the instance variable!

- this method is actually void, so it wont return anything. in order to return the VALUE OF A VARIABLE, we need a get method.

```java
public int getAge(){
return age;
}
```
notice this method does not take anything.

- lets do this with the others.
```java
   public void setColor(String color){
        this.color=color;
    }
    public String getColor(){
        return color;
    }
    
    public void setSound(String sound){
        this.sound=sound;
    }
    public String getSound(){
        return sound;
    }

-yes!
```


    
 - okay, so now we have our updated cat class wtih its setters and getters
 
 -**UPDATED CAT CLASS**
    
```java

    public class Cat {
    // what does a cat have?
    // an age, color, and what sound it makes...

    private int age;
    private String color;
    private String sound;

    // as you can see, we have our instance variables.

    // now we will start with setters.

    public void setAge(int age){
        this.age=age;
    }
    // right now, this method is void- and so it wont return anything

    // so we need a get method to actually GET THE VALUE

    //so
    
    // this is not taking in anything.
    public int getAge(){
        return age;
    }


    public void setColor(String color){
        this.color=color;
    }
    public String getColor(){
        return color;
    }

    public void setSound(String sound){
        this.sound=sound;
    }
    public String getSound(){
        return sound;
    }
}
```
-------------------------------------------------------------------------------------------

- Now we have to work on the **Main** class

- we can introduce a new cat object and **SET** values using the set methods

```java
Cat catone= new Cat();
catone.setAge(13);
catone.setColor("blue");
catone.setSound("meow");
```

- as you can see, we are only setting things and not actually returning anything just yet

- lets print the values using the methods and combine them into one sentence

```java
System.out.println("Hello, this is Catone!, I am " + catone.getAge() + " years old and I am the color " + catone.getColor() + " and I go " + catone.getSound() );
```

this prints out
**Hello, this is Catone!, I am 13 years old and I am the color blue and I go meow**

Great!

-- New updated MAIN class

```java
public class Main {
    public static void main(String[] args) {

        Cat catone= new Cat();

        catone.setAge(13);
        catone.setColor("blue");
        catone.setSound("meow");
// and now we are simply setting a sample cat to be 13 years old, blue, and says meow

        System.out.println("Hello, this is Catone!, I am " + catone.getAge() + " years old and I am the color " + catone.getColor() + " and I go " + catone.getSound());
    }
}
```

---------------------------------------------------------------------------------------------

END OF THIS NOTE
