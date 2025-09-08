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
# Thought process
import what should we have
