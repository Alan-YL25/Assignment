# This is the code:

```java
import java.util.*;

public class frequency
{
    public static int getWordFrequency(String[] wordsList, int listSize, String currWord){
        int count = 0;
        for (int i = 0; i < listSize; i++) {
            if (wordsList[i].equalsIgnoreCase(currWord)) {
                count++;
            }
        }
        return count;
    }
    
    public static void main(String args[]){
        Scanner scan = new Scanner(System.in);
        
        String line = scan.nextLine();

        String[] words = line.split("\\s+");
        int size = words.length;
      
        for (int i = 0; i < size; i++) {
            int frequency = getWordFrequency(words, size, words[i]);
            System.out.println(words[i] + " " + frequency);
        }
    }
}
```
Sorry for not using flowchart and video, maybe I could learn them later

# Thought process
import what should we have at the beginning

First, scan the input, this part should be in the main method, details about it will be explained later. 

Second, define how to write the ```javagetWordFrequency()``` method, as the example output showed, the counting ignore the upper or lower letter, so I use ```java.equalsIgnoreCase()``` to count the frequency.

Third, print out the result as required format, it is at the end of main method and simply use a for loop.

## Frequency analysis for a website
Actually I don't really understand what this question means, as a website include tons of words, and we need to make an analysis for it, maybe we should processing the raw date collected from the website,
after collecting data, manually emphasize some words that containning more information and ignore some words like 'me', 'the'. For example, for a website about the weather change, our analysis should be more 
focusing on words like 'temperature' although words like 'the' are likely appear more frequently.

## Challenge faced
The difficult I've had on this assignment is the scanning part, I've tried to use the read next command (```java.next()```) to put input words into the array one by one, but when I run the code, it comes to a 
infinite loop because it need a manually terminate of inputting by press some key, it make no sense, I replaced it by read nextLine (```java.nextLine()```) as a string, then split them by space and put into the 
array, thus no loop error occurs while inputting.

# How the code work
Some of this part is included in the answers above, in summary, the code scan the input words as a whole string then split them and put into an array, use the array as an argument of a specific method to counting the 
frequency of each word in the array ignore upper or lower letter one by one using a loop, and print out the count one by one in lines until reaches the end of the array.
