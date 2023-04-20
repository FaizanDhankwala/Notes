-This is the Dutch national Problem
----------------------------------------------------------------------

- Given an array of 0,1,2 where 0's represents red, 1s represent white, and 2 represents blue-

-return that same array with all 0's on the left, 1s in the middle, and 2's on the right **WITH ONE PASS* No sorting

Lets start
-----------------------------------------
- in order to complete this problem in one pass, we need 3 pointers. Low, medium, and high.

The low will represent the RED in the flag- or all 0s
the medium will represent the WHITE in the flag- or all 1s
and the high will represent the BLUE in the flag- or all 2s.


so, if we had an array say-

```java
public class dutchpractice {
    public static void dutchpractice(int[] nums){
        
       }
}
```

- AS you can see, we have an unsorted array.

now we can should add the low and high pointer.
The low pointer should be the first element- so nums[0]=low;
and the high pointer should be the last element- so nums.length-1=high;


- the condtion needs to be until the mid pointer reaches the high pointer, the array is not sorted
- But how will we illeterate through the array?

- we will use the mid pointer. IF the mid pointer is 0, we will swap the value with the low pointer and increment the low pointer by one. IF the value is 2, we will switch it with the high pointe and decrement the value of the high pointer


-If the value is one, we will just increment the mid pointer.


We will do this all in one file. So, we can start off with writing the dutch file.

```java
public class dutchpractice {
    public static void dutchpractice(int[] nums){
    int low= 0; // both low and mid are at the first positon of the array.
    int mid=0;
    int high= nums.length-1; // and high is at the last poistion
        
       }
}
```


- we need a while loop

 ```java
public class dutchpractice {
    public static void dutchpractice(int[] nums){
    int low= 0; 
    int mid=0;
    int high= nums.length-1; 
    
    while(mid<=high){//while mid is less or equal to high
    
    switch(nums[mid]){// switching nums with mid.
    
    case 0: {
    swap( nums, mid, low);// swap mid and low
    mid++;
    low++;
    break;
    }
    case 1:{ // just move on
    mid++;
    break;
    }
    case 2: {
    swap( nums, mid, high); // swap mid and high 
    high--;
    break;
    
        
       }
}
```
-Now we need to write the swap() method.
- this method will take an array and two variables as parameters
```java
public static void swap(int[] array1, int first, int second){

int temp= array1[first];
array1[first]=array1[second];
array1[second]=temp;
```


-and now we need a print function for the array
this will take an array as a paremter
```java
public static void printarray(int [] array1){

for int (nums: array1){
System.out.print(nums + " " );
}
```

- and now the main to call everything

```java
public static void main(String[] args){

int [] nums= {1,2,2,0,0,0,1,2};

dutchpractice(nums);
printarray(nums);
```

FULL FILE

```java




public class dutchpractice {
    public static void dutchpractice(int[] nums) {
        int low = 0;
        int mid = 0;
        int high = nums.length - 1;

        while (mid <= high) {//while mid is less or equal to high

            switch (nums[mid]) {// switching nums with mid.

                case 0: {
                    swap(nums, mid, low);// swap mid and low
                    mid++;
                    low++;
                    break;
                }
                case 1: { // just move on
                    mid++;
                    break;
                }

                case 2: {
                    swap(nums, mid, high); // swap mid and high
                    high--;
                    break;


                }
            }
        }
    }


    private static void swap(int[] array1, int first, int second) {

        int temp = array1[first];
        array1[first] = array1[second];
        array1[second] = temp;

    }






                            public static void main(String[] args) {

                                int[] nums = {1, 2, 2, 0, 0, 0, 1, 2};

                                dutchpractice(nums);
                                printarray(nums);
                            }


                    public static void printarray(int [] array2){

                        for(int nums: array2){
                            System.out.print(nums + " " );
                        }
                    }
                }

```

Output

**0 0 0 1 1 2 2 2 **






