## Lab Report - 5
June 10, 2024

# Part 1 – Debugging Scenario

1. **Original Student Post**
   I have a `ListExamples.java` file with a merge funciton and `TestListExamples.java` file to test the merge function. However, when I try to run the bash file which compiles both files and runs the junit tests, it tells me it couldn't find `test.sh` and fails my tests, even though they seem to work when I run them directly on VSCode.
![Image]()

2. **TA Response**
   Good idea on trying to run the tests directly on VSCode! This means your code is probably correct in the `.java` files. Try checking your `test.sh` file again and make sure you are using the correct arguments with it in the command line.

3. **Final Student Post**
   I realized I was using the wrong variable in the last line of `test.sh`. `$0` actually gives the name of the file, the correct first argument should actually be `$1`. Thank you so much!
  ![Image]()

4. **All Information:**
  - Three files created called `ListExamples.java`, `TestListExamples.java`, and `test.sh`.
  - `ListExamples.java` content:
    ```
    /**
 * Copied from list-examples-grader from cse15L spring'24
 */
import java.util.ArrayList;
import java.util.List;

class ListExamples {
    
  // Takes two sorted list of strings (so "a" appears before "b" and so on),
  // and return a new list that has all the strings in both list in sorted order.
  static List<String> merge(List<String> list1, List<String> list2) {
    List<String> result = new ArrayList<>();
    int index1 = 0, index2 = 0;
    while(index1 < list1.size() && index2 < list2.size()) {
      if(list1.get(index1).compareTo(list2.get(index2)) < 0) {
        result.add(list1.get(index1));
        index1 += 1;
      }
      else {
        result.add(list2.get(index2));
        index2 += 1;
      }
    }
    while(index1 < list1.size()) {
      result.add(list1.get(index1));
      index1 += 1;
    }
    while(index2 < list2.size()) {
      result.add(list2.get(index2));
      index2 += 1;
    }
    return result;
  }
}
    ```
  - `TestListExamples.java` content:
    ```
    import static org.junit.Assert.*;
import org.junit.*;

import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class TestListExamples {

  @Test(timeout = 500)
  public void testMergeRightEnd() {
    List<String> left = Arrays.asList("a", "b", "c");
    List<String> right = Arrays.asList("a", "d");
    List<String> merged = ListExamples.merge(left, right);
    List<String> expected = Arrays.asList("a", "a", "b", "c", "d");
    assertEquals(expected, merged);
  }

  @Test
  public void testMergeEmpty1() {
    List<String> left = Arrays.asList("a", "b", "c");
    List<String> empty = new ArrayList<>();
    assertEquals(ListExamples.merge(left, empty), left);
  }

  @Test
  public void testMergeEmpty2() {
    List<String> leftEmpty = new ArrayList<>();
    List<String> rightEmpty = new ArrayList<>();
    assertEquals(ListExamples.merge(leftEmpty, rightEmpty), leftEmpty);
  }

}
    ```
    
  - `test.sh` content:
    ```
    CPATH='.:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar'

javac -cp $CPATH ListExamples.java TestListExamples.java 

if [[ $? == 0 ]]
then 
    echo "Files successfully compiled"
else 
    echo "Files did not successfully compile"
    exit
fi

java -cp $CPATH org.junit.runner.JUnitCore $0
    ```

  - Command line to trigger bug : `adyasachdev@Adyas-MacBook-Air labreport_5 % bash test.sh TestListExamples`
  - To fix bug : edited line 13 of `test.sh` file to take the first arguement from the command line i.e from `$0` to `$1`. 


# Part 2 – Reflection
I enjoyed learning about bash scripts and how to use them in lecture and lab. It was very intereseting to see the amount of commands you could carry out by writing them in the bash script i
