# Big O Notation

When it comes to code, we have many ways to write it. Each person will bring their own set of knowledge and this field is highly opinionated so how do we know which code is good? We can summarize writing code into 2 things: **readability** and **scalability**. 

**Readability** simply means that if another developer (or you after some time) looks at your code, they should be able to understand it. This means that it is logical, makes sense and follows the best practices. For python we use [PEP 8](https://peps.python.org/pep-0008/) style guide to help us write code that is consistent and so any python developer that comes across our code should be able to read it!

**Scalability** is where it gets interesting. If I write a piece of code, it should be able to run efficiently regardless of whether the input is small or not. If the input size is only 100, we might not feel that but as our input size increases to 100,000 or 100,000,000 does that code still run efficiently? This is where Big O comes in. It helps us determine if the code we are writing is optimized or not. With scalability, our main concern becomes about **time** (speed) and **space** (memory). 

Big O is how we analyze our code to determine the efficiency of the code we right. This really helps us become better programmers because it makes us think differently about the code we are writing. What Big O really tells is how our code will behave for a very large input size or we can say it is the rate at which our algorithm grows in relation the the input.

Below is a graph that outlines that main Big O complexities and I've highlight what they mean and the most common ways you might encounter each in the chart below.

![Big O Graph](../resources/BIG%20O%20Graph.png)

| BIG O | Meaning | What it commonly means in code |
|-------|---------|-----------------------|
| O (1) | Constant | Variables, if/else statements, return statements etc. |
| O (log n) | Logarithmic | base 2, how many times we must divide/multiply by 2 to get answer |
|O (sqrt(n)) | Square root |  |
| O (n) | Linear | For loop |
| O (n log n) | Log Linear | Sorting |
| O (n^2) | Quadratic | Nested for loop, go through all pairs |
| O (2^n) | exponential | recursive algorithms, O (branches^depth) |
| O (n!) | factorial | Loop for every element |

## Calculating Big O

There are 3 scenarios we can look at when we analyze an algorithm, the best case, the average case and the worst case. If I use the best or average case as a measuring stick, it wouldn't really be an effective way since our algorithm could perform a lot worse in it's worse scenario but if our algorithm is effecitve in it's worst case, it will always perform better in the average and best case. So we are only concerned with the worse case since that is the upper bound. To calculate Big O we simply read the block of code line by line and assign values for each operation. The general rule of thumb is to use multiply for loops and addition otherwise.

#### Rules for Big O
1. Worst case only
2. Remove constants
3. Use different terms for different inputs
4. Drop non-dominant terms

#### Amortized Time

This is also an important thing to consider but isn't discussed as much because it's not very common. Consider the array data structure. Everytime you append a new element in an array, the cost to do that is O (1). But what happens when that array reaches full capacity? At n items, appending a new element is O (n + 1). You have to create a new array which is done dynamically (the array size doubles when reaching capacity). Then you have to copy all the elements to the new array which is O (n) and lastly you append the new element O (1). So every append is O (1) except when the array is full. But the resizing of array happens so rarely that it can be neglected and amortize the cost as O (1).
