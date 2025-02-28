# Big O Notation

When it comes to code, we have many ways to write it. Each person will bring their own set of knowledge and this field is highly opinionated so how do we know which code is good? We can summarize writing code into 2 things: **readability** and **scalability**. 

Readability simply means that if another developer (or you after some time) looks at your code, they should be able to understand it. This means that it is logical, makes sense and follows the best practices. For python we use [PEP 8](https://peps.python.org/pep-0008/) style guide to help us write code that is consistent and so any python developer that comes across our code should be able to read it!

Scalability is where it gets interesting. If I write a piece of code, it should be able to run efficiently regardless of whether the input is small or not. If the input size is only 100, we might not feel that but as our input size increases to 100,000 or 100,000,000 does that code still run efficiently? This is where Big O comes in. It helps us determine if the code we are writing is optimized or not. With scalability, our main concern becomes about **time** (speed) and **space** (memory). 

Big O is how we analyze our code to determine the efficiency of the code we right. This really helps us become better programmers because it makes us think differently about the code we are writing.

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
| O (2^n) | exponential |  |
| O (n!) | factorial | Loop for every element |