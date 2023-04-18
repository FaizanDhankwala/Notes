Removing duplicates from a sorted array
------------------------------------------------

-This note will cover how to remove duplicates in a given sorted array.
- Lets start.

So say, you wanted to remove duplicates in a sorted array and return the number of UNIQUE elements in the array.
**Let me explain**

For example,
if you had the array-
```java
int[]numbers={1,1,1,2,3,4,4,5,6};
```
If you were to remove all duplicates, the output would be
```java
1,2,3,4,5,6
```
and the amount of unique elements would be 6.

- How do we do this in code?????????????????????????!!

-Its quite simple. We will need 2 pointers. Basically 2 variables that do different things One of them will be called the slowpointer and one will be the fastpointer.

The slow pointer will start at the FIRST element of the array- so basically numbers[0]. This number, will always be unique- because it is sorted after all, and so the first number will be unique.

- The fast pointer will be put in a loop that will illeterate through the entire array and compare each number to whatever number the first pointer is looking at.

-Lets take a lookkk
-------------------------------

```java
  public static int removeDuplicates(int[] numbers) {
  //slow pointer and it is being set to the first index of the array
  int slowpointer=0;
  // for loop with the second index being set the to second element of the array
  for{int fastpointer=1; fastpointer<numbers.length; fastpointer++){
  
  }
  ```
  
  -As you can see, we have the two pointers set up. Now whats the logic that we need to place??
  
  -we first have to compare the number the fast pointer is on to the one the slow pointer is looking at. Are they the same? If so, skip it. Are they different?
  If so, place it to wherever the slowpointer is +1- the next spot basically.
  
  So
  
  ```java
  public static int removeDuplicates(int[] numbers) {
  //slow pointer and it is being set to the first index of the array
  int slowpointer=0;
  // for loop with the second index being set the to second element of the array
  for{int fastpointer=1; fastpointer<numbers.length; fastpointer++){
  
  // if whatever number slowpointer is- is  NOT equal to whatever number fast pointer is...
  if(numbers[slowpointer]!=numbers[fastpointer]{
  //THEN, whatever the number one after slow pointer becomes the number fast pointer was looking at. This way, they become sorted
  numbers[++slowpointer]= numbers[fastpointer];
  }
  ```
  
  -And now we need to find out how many unique elements were there.
  - But what you dont realize is that slowpointer has been incremented all this time. It will increment hwoever many times a new unique element is introduced.
  - This means that we can just return slowpointer + 1 to count for the last elemet and this should be the amount of unique elements. 

-so 

```java
  public static int removeDuplicates(int[] numbers) {
  //slow pointer and it is being set to the first index of the array
  int slowpointer=0;
  // for loop with the second index being set the to second element of the array
  for{int fastpointer=1; fastpointer<numbers.length; fastpointer++){
  
  // if whatever number slowpointer is- is  NOT equal to whatever number fast pointer is...
  if(numbers[slowpointer]!=numbers[fastpointer]{
  //THEN, whatever the number one after slow pointer becomes the number fast pointer was looking at. This way, they become sorted
  numbers[++slowpointer]= numbers[fastpointer];
  }
  }
  return slowpointer+1;
  }
  ```
  -!!!!
