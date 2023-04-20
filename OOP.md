-This note will allow us to learn some terms in Object oriented PRogramming
------------------------------------------------------

The Copy Constructor function
-----------------------------------------

-Say you had an Object  "A", and you had a second object "A" again. And they were exactly the same except the second A is not the first A.


How would we do this?
-Lets choose a simpler idea.

Say you had a enemy class from a video game.

```java
public class Enemy {
    private String name;
    private String[] weapons;
    private int hitpoints;
}
```

- Then in the main, we can define two enemies and set one to the other

```java
public class Main {
    public static void main(String[] args){

Enemy George= new Enemy();

Enemy Felecia= George;


    }
}
```

Felecia has all of George's traits right?

**WRONG**
-This does not make a new instance of the class, rather assigns two enemy variables pointing at the same enemy

- we need to create a copy constructor in java.

