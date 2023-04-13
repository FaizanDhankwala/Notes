Overiding
--------------------------------
- this note will cover method overiding
- lets start

- So we first start off with an animal class

```java
public class Animal {
    
}
```

- and in this class, it has one method- a speak method

```java
public class Animal {
    void speak(){
    System.out.println("The animal speaks");
}
```

-next we will have a dog object (a class esentially) that extends animal.

```java
public class Dog extends Animal{
    
}
```
And now in our main, we will create  a dog object and make it use the speak method

```java
public class Mainoveriding {
    public static void main(String[] args){
    Dog dogone = new Dog();

    dogone.speak();
}
}
```
- if you would run this in main it would print out

**The animal speaks**

now, if we put the speak method into the dog class itself this is called overiding.

```java
public class Dog extends Animal {
    void speak() {
        System.out.println("the animal speaks");
    }
}
```
Here is what it looks like now

- we should proably change it so it resembles a dog more.


```java
public class Dog extends Animal {
    void speak() {
        System.out.println("the dog barks");
    }
}
```
-- now if we run main, we get
** the dog barks**

because we overode a method, it is good practice to put @overide above the method

YAYA

NOTE END
