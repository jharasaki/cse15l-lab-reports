# Lab Report 5 - Putting it All Together

## Part 1 – Debugging Scenario

1.) Original Post:

  Subject: "Issue with Merging Lists in Java"

"Hello,

I'm currently working on a Java program that is supposed to calculate the average of a list of integers. When I run grade.sh to calculate the average of the numbers 10, 20, and 30, I expect the result to be 20, but the output is showing that the average is 30.0. What could be wrong with my AverageCalculator.java?"

Here is the code:
```
import java.util.ArrayList;

public class AverageCalculator {
    public static double calculateAverage(ArrayList<Integer> numbers) {
        double sum = 0;
        for (int num : numbers) {
            sum += num;
        }
        return sum / (numbers.size() - 1);
    }

    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<>();
        numbers.add(10);
        numbers.add(20);
        numbers.add(30);
        System.out.println("Average: " + calculateAverage(numbers));
    }
}
```

Output:

<img width="561" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/e607d245-dc51-48a9-819f-369d70d5b64c">


2.) TA Suggestion: "It seems like there could be an issue with how you're calculating the average. Can you insert a print statement to display the value of sum and the count of numbers (numbers.size()) before the division? This will help us diagnose the issue."


3.) Here is the student trying the TA's suggestion:
```
import java.util.ArrayList;

public class AverageCalculator {
    public static double calculateAverage(ArrayList<Integer> numbers) {
        double sum = 0;
        for (int num : numbers) {
            sum += num;
        }
        System.out.println(numbers.size());
        return sum / (numbers.size() - 1);
    }

    public static void main(String[] args) {
        ArrayList<Integer> numbers = new ArrayList<>();
        numbers.add(10);
        numbers.add(20);
        numbers.add(30);
        System.out.println("Average: " + calculateAverage(numbers));
    }
}
```

Output:

<img width="848" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/f21dda3f-c66e-482e-afe4-719b59634cd1">

4.) Setup Information

  File & Directory Structure:
    |-lab9
    |    |-AverageCalculator.class
    |    |-AverageCalculator.java
    |    |-grade.sh

  Contents of Each File Before Fixing: Shown in 1.
  Full Command Line to Trigger the Bug: `bash grade.sh`
  Description of What to Edit to Fix the Bug: In AverageCalculator.java, change return sum / (numbers.size() - 1); to return sum / numbers.size(); to correctly calculate the average.

<img width="389" alt="image" src="https://github.com/jharasaki/cse15l-lab-reports/assets/156235690/ed7fb3ea-c0bc-435c-8b2f-3e861e5098ac">



## Part 2 - Reflection

The coolest part of this second half for me was probably using Vim to do almost do everything just from the command line. Especially for really long files I may deal with in the future, the commands in Vim could be really useful in saving time. To be honest, other than that, I am not sure yet how helpful it could be for me but there were a lot more tools and commands that I could use that even up my efficiency even more.


