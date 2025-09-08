# This is the code:

```java

import java.util.*;

public class Sorting
{
    public static void sortArray(int[] myArr, int arrSize){
        for(int i = 0; i < arrSize - 1; i++){
            for(int j = 0; j < arrSize - i - 1; j++){
                if(myArr[j] < myArr[j + 1]){
                    int temp = myArr[j];
                    myArr[j] = myArr[j + 1];
                    myArr[j + 1] = temp;
                }
            }
        }
    }

    public static void main(String args[]){
        Scanner scan = new Scanner(System.in);
        int size = scan.nextInt();
        int[] nums = new int[size];
        for(int i = 0; i < size; i++){
            nums[i] = scan.nextInt();
        }

        sortArray(nums, size);

        for (int i = 0; i < size; i++) {
            System.out.print(nums[i]);
            if(i != size - 1){
                System.out.print(",");
            }
        }
        System.out.println();

    }
}
```

Sorry for not using flowchart and video here, maybe I will learn them later

# Thought process
import what we should have at the beginning
First, the code should able to scan the input, the only thing should be noticed is the first numbers is the size of array which not included in that, then use nextInt() to scan numbers in array, this part should be in the main method.
Second, create a method that could re-order the array from the argument by descenging order, I will explain this part in the how the code works part.
Third, print the re-ordered array with required format, this part is in the end of main method.

## Why I choose this
Because I think this is the simpliest code I can write, it is good for the efficiency of coding and reading.

## Challenge faced
I see there is a simple ```javaArrays.sort()``` I can use, but it is only work on ascending order, after trying, I found that if I want a descending order one with this ```javaArrays.sort()```, 
I need to creat a new array and write a loop to reverse the original array, it is more complicated and hard to read so I chose the format above. Comparing two ways this the challenge I faced.
Edit: maybe I don't need a new array, create a temp variable is enough, but it is similar to the current code.

# How the code works
The main method is scanning input and print result, this method is easy, scan the size and content of an array then put them into sorting method as arguments, after sorting method runs, print the result.
The key is the sorting method, I use a nested loop to re-order the array, this compares two adjacent numbers, when the previous one is smaller, using a temp int variable to switch their places to make sure the array is in descending order 
until reaches the end of the array.
