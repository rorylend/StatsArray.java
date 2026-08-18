
## 🟣 StatsArray.java

**Description**
This program creates an array of integers named `scores` with a size of 10. It fills the array with random numbers in the range of 0–100, then calculates the total of all values, the average, the largest value, the smallest value, and how many numbers fall between 90 and 100 inclusive. The inputs are numbers from the random number generator. The outputs are the exam scores, the minimum value, the maximum, the total, the average, and the number of A's.

**Tech Stack**
- Language: Java
- Tool/Library: Eclipse

<details>
<summary>💻 Show code</summary>

```java
/** Hi.java
 *  Rory Lendzion
/** CSC110
/** 6/25/2026
import java.util.Random;
public class StatsArray {
	public static void main(String[] args) {
		int[] scores = new int[10]; //an array of integers named scores with size 10
		Random rand = new Random();
		
		//use random class to fill the scores array with random  numbers 0-100
		for (int i =0; i < scores.length; i++) {
			scores[i] = rand.nextInt(101); //generates integers 0 to 100
		}
		
		//display the array elements
		System.out.println("Exam Scores");
		System.out.println("-----------");
		for (int i = 0; i < scores.length; i++) {
			System.out.println("[" +i + "] " + scores[i]);
		}
		
		//initialize variables
		int total = 0;
		int max = scores[0];
		int min = scores[0];
		int countA = 0;
		
		//use the array to find stats
		for (int score : scores) {
			total += score; //calc total
			
			if (score > max) {
				max = score; //find largest
			}
			
			if (score < min) {
				min = score; //find smallest
			}
			
			if (score >= 90 && score <= 100) {
				countA++; // Count numbers between 9 and 100 inclusive
			}
		}
		
		//calc the average
		double average = (double) total / scores.length;
		
		//display all of the statistics
		System.out.println("The minimum value : " + min);
		System.out.println("The maximum value : " + max);
		System.out.println("The total is      : " + total);
		System.out.println("The average is    : " + average);
		System.out.println("Number of A's     : " + countA);
		System.out.print("Goodbye!");
	}
}
```

</details>

**Usage**
Example output (values are randomized each run):

<details>
<summary>💻 Show expected output</summary>

```java
Exam Scores
-----------
[0] 59
[1] 69
[2] 84
[3] 75
[4] 90
[5] 86
[6] 97
[7] 53
[8] 14
[9] 17
The minimum value : 14
The maximum value : 97
The total is      : 644
The average is    : 64.4
Number of A's     : 2
Goodbye!
```

</details>

---

## 📚 What I Learned

Arrays, loops, the Random class, enhanced for loops, and calculating basic statistics from array data.


