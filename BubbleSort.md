BubbleSort
------------------------------------------------
- This note will cover the epic topic of bubble sort
Lets start
--------------------------------------------
- bubble sort will sort elements in asceding order

So first, we need to know that in order to switch two things around- we need a third variable we will call this

```java
int temp;
```
The bubble sorting algortim takes foerevr to do long sorts

anyway lets start with a main

```java
public static void main(String[] args){

}
```
-In here, we will need an array
```java
public static void main(String[] args){
int array1[]={4,2,1,9,7,10,2};
}
```
-Now lets put a for loop in it to display values!
```java
public static void main(String[] args){
int array1[]={4,2,1,9,7,10,2};
for(int i: array1){
System.out.print(i);
}
```
-This will print
**42197102**
As you can see this is not in order at all.
- Lets sort it!
- we can now declare a bubblesort() method outside of our main method.
- - this array will take one parameter- an array
```java
public static void main(String[] args){
int array1[]={4,2,1,9,7,10,2};
for(int i: array1){
System.out.print(i);
}
public static void bubbleSort(int array[]){

```

- In this method, there will be a nested for loop

```java
public static void bubbleSort(int array[]){
for(int i= 0; i<array.length-1; i++){
for(int j=0; j<array.length-i-1; j++){
if(array[j]>array[j+1]){
int temp= array[j];
array[j]=array[j+1];
temp=array[j+1];
}
}
```
This returns
**12247910**

-Lets explain

-AFter the nested loop, 

**If array[j], the number on that spot is GREATER than the number right after it( array[j+1]), then a temproray variable named temp will take the value of array[j].
Then, array[j] which is now empty (has no value) is reassigned to array[j+1] 
Lastly, temp's value is given back to array[j+1]**

Its that simple!
