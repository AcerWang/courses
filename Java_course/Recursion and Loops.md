# Recursion & Loops

## 1. Experiment Introduction

Computers are often used to automate repetitive tasks. Repeating tasks without making errors is something that computers do well and people do poorly. Like conditional expressions, loops also can be nested one in another, but this will make our program hard to read and the performance is not good, try to get avoid of nested loops. There are three types of recursion in Java, we'll learn one by one in this lab.

### Learning Objective

- Recursion & Loops
  - while loop
  - do-while loop
  - for loop

## 2. Content
Recursion in computer science is a method where the solution to a problem depends on solutions to smaller instances of the same problem (as opposed to iteration). The approach can be applied to many types of problems, and recursion is one of the central ideas of computer science. The power of recursion evidently lies in the possibility of defining an infinite set of objects by a finite statement. In the same manner, an infinite number of computations can be described by a finite recursive program, even if this program contains no explicit repetitions.
**Example**

```
public class recursionTest{
    public static int fibonacci(int n){  
        if(n<=2){  
            return 1;  
        }else{
            return fibonacci(n-1)+fibonacci(n-2);  
        }  
    }
    public static void main(String[] args){
        int res = recursionTest.fibonacci(10);
        System.out.println(res);
    }
}
```
**Output:**

```
55
```
![image desc](https://labex.io/upload/X/V/E/7ipNh183q9Og.png)
### 2.1 while loop

When entering the while loop, firstly the condition will be checked. The while loop will always run until the condition is false. The syntax is like this:

**Example**

```
public class whileTest
{
    public static void main(String[] args)
    {
        int x = 1;
        // exit when x is bigger than 3, the inner code will run 3 times in all.
        while (x <= 3)
        {
            System.out.println("x = " + x);
            // increment the value of x by 1 each time for next iteration
            x++;
        }
    }
}
```

**Output:**

```
x = 1
x = 2
x = 3
```

![image desc](https://labex.io/upload/C/O/Q/HN62f4IqOUar.png)

### 2.2 do-while loop

This loop is very similar to the while loop, but there is one difference. whatever the condition is, the loop will always run once, then the condition is checked. So sometimes, maybe it's not fit for some circumstances. The syntax is :

**Example**

```
public class doWhileTest
{
    public static void main(String[] args)
    {
	    int x = 1;
	    do
	    {
		    // the code below will run first, then condition is checked.
		    System.out.println("x = " + x);
		    x++;
	    }
	    while (x <= 3);
    }
}
```

**Output**​

```
x = 1
x = 2
x = 3
```

![image desc](https://labex.io/upload/F/T/A/KWQgfhT1iSdC.png)

### 2.3 for loop

The for loop looks like this:

**Example**

```
for (init expression; condition expression; sub expression)
{
	// statements here
}
```

The init condition marking the start of a for loop, will run only once. Condition expression will be checked each time before enter the loop, it is used for testing the exit condition for a loop and must return a boolean value. Once the condition is true, the statements in the loop are executed, then the sub expression will be executed.

**Example**

```
public class forTest
{
    public static void main(String[] args)
    {
	    // for loop begins when x=1 till x<=3
	    for (int x = 1; x <= 3; x++) {
	    	System.out.println("x = " + x);
		}
	}
}
```

**Output:**    

```
x = 1
x = 2
x = 3
```

![image desc](https://labex.io/upload/C/O/W/qnERcqBOSKQA.png)

You can exit the loop whenever you want in the loop body by using code like continue, break in a if condition. break will exit the whole loop while continue will only quit the current loop and do next iteration.

**Example**

```
public class loopTest
{
    public static void main(String[] args)
    {
	    // for loop begins when x=1 till x<=3
	    for (int x = 1; x <= 3; x++) {
			if(x==2){
				// exit the whole loop
			    break;
				// continue will only quit the current loop, and do next iteration
			    // you can delete the break expression and use continue, see the output.
                // continue;
			}
	    	System.out.println("x = " + x);
	    }
	}
}
```

**Output:**  

```
x = 1
```

![image desc](https://labex.io/upload/E/L/R/bTq0tztrtCct.png)



## 3. Summary

In this lab, we learned three loops, for loop and while loop are common, do-while loop is not very perfect logically, you should choose it very carefully. Now you can try an advanced trial, use these knowledge of this lab and last lab, and binary method to complete a small game: [Guess number higher or lower](https://leetcode.com/problems/guess-number-higher-or-lower/).