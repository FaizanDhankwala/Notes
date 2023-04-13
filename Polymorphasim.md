Polymorphasim
---------------------------------

- this note will be about Polymorphasim.
-  In this example, we will only have one file.
-  In the file, there will be multiple classes however

Lets Begin
---------------------------

- We need a new class
```java
public class polymorphism {
    public static void main(String[] args){

        
    }
}
```
Intresting

- but in this class we need another class right above it. In the same file!
- We will call this cookies

```java
class Cookies{
    
}

public class polymorphism {
    public static void main(String[] args){


    }
}
```

Now we have our updated class

- lets add a method to the cookie class. This will simply print osmething

 ```java
public void dip(){
    System.out.println("milk milk milk");
}
```
Next we can put this object into the main method

```java

public class polymorphism {
    public static void main(String[] args) {

        Cookies chocoloate = new Cookies();
        chocoloate.dip();
    }
}
```
Ok great
BUT!
What if we had another class cookie that had the same dip method???

Intresting. A challenge!

- for this we will introduce a new cookie type class - and OREO

```java
class Oreo{
  public void dip(){
        System.out.println("milk milk milk");
    }
```
As you can see, the two methods have the smae dip() function.

that is one way- by just doing that or we could use 
extends
---------------------------------
take a look
```java
lass Cookies{
public void dip(){
    System.out.println("milk milk milk");
}

class Oreo extends Cookies{

    
}
    }



public class polymorphism {
    public static void main(String[] args) {

        Cookies chocoloate = new Cookies();
        chocoloate.dip();
    }
}
```

-We can then change the main function into an oreo.
Take a look
```java
public class polymorphism {
    public static void main(String[] args) {

        Oreo chocoloate = new Oreo();
        chocoloate.dip();
    }
}
```

If we run this we get,
**milk milk milk**

As you can see, without even providing another print statmenet we simply have made a class that extends another and it returns the same thing. Lets add more now

-The thing is that not all cookies go good with milk. Some go good with tea. So we need the same dip method- but with different values inside? hmmm lets do this

Same Methods, Different Values
------------------------------------------
- So an Oreo would go good with cholate milk and a sugar cookie would go good with tea

so lets put the same dip method into them
```java
class Oreo extends Cookies{
    public void dip() {
        System.out.println("chocolate milk");
    }


}

class Sugar extends Cookies{
    public void dip() {
        System.out.println("Tea missiou");
    }

}
```
Now they have different values

- Now if say the class "oreo" knows 2 dip methods. One from its own and one from the cookies class. Which one will it print?
- So if we call it in main

```java

public class polymorphism {
    public static void main(String[] args) {

        Oreo chocoloate = new Oreo();
        chocoloate.dip();
    }
}
```
This will return
**chocolate milk**

Because it priorities the class it is in

THATS IT

END OF NOTE
