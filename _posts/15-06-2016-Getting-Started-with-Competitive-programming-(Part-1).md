---
layout: post
title: Getting Started with Competitive Programming (part 1)
cover: 'assets/images/Code.jpg'
tags: Algorithms,Programming,Tutorial
subclass: 'post '
navigation: True
---



<h4>Hey Folks!</h4>

This is my first blog post in the series. This series is going to be about how and why you should get started in competitive programming. Since a lot of my friends were asking what to do in summers, This can be one thing to start.

Let's get started!

<h4><b><i>Q1) What is it?</i></b></h4>

Well, According to Wikipedia :

> Competitive programming is a mind sport usually held over the Internet or a local network, involving participants trying to program according to provided specifications. Contestants are referred to as sport programmers.

In layman terms, Competitive programming is like a math competition. We have to solve easy/hard problems in a given amount of time. Like math problems, except based on topics around computer science and written in some word context. It is really more fun than it sounds. :)

<h4><b><i>Q2) How is competitive programming different from Real-world programming?</i></b></h4>

I found this awesome answer on _[Quora](https://www.quora.com/How-is-competitive-programming-different-from-real-life-programming)_ for this question.

Here it goes,

>**You are in the jungle. You have a pocket-knife.** Someone asks you to kill a mountain lion.
>
Years of training has taught you well. You use your knife to sharpen a stick. You cut vines to lash sharp stones on one end. Maybe you're from a top university, and you've learned to extract essential ingredients from plant and insect life around you to fashion a poison to tip your weapon with. 
>
Convinced that you have an effective and efficient way to kill the lion, you set forth to accomplish your task. Maybe your stick is too short, or your poisons don't work. It's okay - you live to refine your method and try again another day.
>
That's "real-life" programming.
>
In competitive programming, you start out with the same resources (a pocket-knife), **except you have 2 minutes to kill the lion.**

I think that answers the question well.


<h4><b><i>Q3) Why should I do it?</i></b></h4>

I'm gonna do this in the pros and cons style.

**_Pros :_**

*  You get better at applying theoretical concepts like Data structures, Dynamic Programming, Graph theory etc.

* You learn how to write optimized code in less time and do team work under pressure.

* Since many of the companies, in their placement procedure test the knowledge of Data-structures and Algorithms along with others, So it is a great practice.

* It is an exercise for brain like playing chess.

* Being high-rated in competitions gives you respect and cool free T-shirts. :)

* It's really fun.

**_Cons :_**

* You are just automating the solution to a logic problem. You aren't building something people will use.

* You get used to creating something good enough to pass the tests in a short period of time, rather than continuously improving an open problem/issue.


<h4><b><i>Q4) Okay enough Chit-chat.. Where do I start?</i></b></h4>

Prerequisites: 

* A lot of Self-Motivation.
* Basics of any programming language. C/C++/JAVA (your choice).
  * We will focus on C++. JAVA is slow.
  * C++ is like a super set of C with some additional tools. If you know C then you know how to code in C++. If not, please revise C (CS101). 
* Get familiarized  with the libraries the language has to offer. Like in C++ learn the Standard template library ([STL](http://www.sgi.com/tech/stl/)).

---

**PRACTICE! PRACTICE! PRACTICE!** (It's the only _mantra_ )

1. <a href="http://www.spoj.com/">SPOJ</a>:  It's an online judge recommended for all beginners.
  *  Firstly, sort the problems with maximum submissions. Solve some problems (maybe 20). Build some confidence. This may seem a daunting task at first but stay motivated.
  * Never get stuck for too long in the beginning. Google your doubts or try to sort them out by discussing it with someone. (**ONLY IN THE BEGINNING**) 
  * Before getting into contests held in codechef or codeforces, make sure you have solved atleast 40-50 problems on SPOJ.
2.  <a href="http://www.codechef.com">CodeChef</a>: Do all the 3 contests every month.
   * Even if you are unable to solve a problem, do look at the editorials and try to get it accepted.
   *  And even if you are able to do it, still look at the codes of some good coders. See how they have implemented.
   * Same points apply for codeforces and topcoder.

3.  <a href="http://www.codeforces.com/">Codeforces</a>: 4 to 5 short contests of 2-3 hours a month (Do this after building some confidence).
4. <a href="http://www.topcoder.com">Topcoder</a>: Once you have proper experience and you can write codes very fast.


<h4><b><i>Q5) Okay..but how do I do those?</i></b></h4>

You write codes and submit them online. The judge runs your code with several test inputs and gives results based on the outputs.

You must follow exact I/O (_Input/output_) format. Please do not put statements like "Please Enter a number " ,etc. :P

Every problem has constraints.
Properly analyse the constraints before start coding:

* Time limit in seconds gives insight on the order of the solution needed (discussed later). 
* The Constraints on Input (Very Important).
* Memory Limit (do not bother unless you are using an insane amount of memory).

Let us consider below problem statement as an example.

**Problem Statement**: (Linear Search) Given an integer array and an element x, find if element is present in array or not. If element is present, then print index of its first occurrence. Else print -1.

**Input** :First line contains an integer, the number of test cases ‘T’. Each test case should be an integer. Size of the array ‘N’ in the second line. In the third line, input the integer elements of the array in a single line separated by space. Element X should be inputted in the fourth line, i.e., after entering the elements of array. Repeat the above steps second line onwards for multiple test cases.

**Output** : Print the output in a separate line returning the index of the element X. If the element is not present, then print -1.

**Constraints**: 
1 <= T <= 100
1 <= N <= 100
1 <= Arr[i] <=100

**Example Input and Output for your program**: 
<pre>
Input:
2
4
1 2 3 4
3
5
10 90 20 30 40
40
Output:
2
4
</pre>
**Explanation** :
<pre>
There are 2 test cases (Note 2 at the beginning of input)
Test Case 1: Input: arr[] = {1, 2, 3, 4},  
                    Element to be searched = 3.
             Output:  2
             Explanation: 3 is present at index 2.

Test Case 2: Input: arr[] = {10, 90, 20, 30, 40}, 
                    Element to be searched = 40.
             Output:  4
             Explanation: 40 is present at index 4.

</pre>

The Following is a C implementation of the solution: 
{% highlight c %}
// A Sample C program for beginners with Competitive Programming
#include<stdio.h>
 
// This function returns index of element x in arr[]
int search(int arr[], int n, int x)
{
    int i;
    for (i = 0; i < n; i++)
    {
       // Return the index of the element if the element
       // is found
       if (arr[i] == x)
         return i;
    }
 
    //return -1 if the element is not found
    return -1;
} 
 
int main()
{
    // Note that size of arr[] is considered 100 according to
    // the constraints mentioned in problem statement.
    int arr[100], x, t, n, i;
 
    // Input the number of test cases you want to run
    scanf("%d", &t); 
 
    // One by one run for all input test cases
    while (t--)
    {
        // Input the size of the array
        scanf("%d", &n); 
 
        // Input the array
        for (i=0; i<n; i++)
           scanf("%d",&arr[i]);
 
        // Input the element to be searched
        scanf("%d", &x);
 
        // Compute and print result
        printf("%d\n", search(arr, n, x));
    }
    return 0;
}
{% endhighlight %}
**Common mistakes by beginners**: 
 
*  Program should not print any extra character. Writing a statement like printf("Enter value of n") would cause rejection on any platform.

* Input and output format specifications must be read carefully. For example, most of the problems expect a new line after every output. So if we don’t write printf(“\n”) or equivalent statement in a loop that runs for all test cases, the program would be rejected.



Okay so that brings us to end of this post. In the next blog post I'll cover the various data-structures and algorithms used in Competitive programming as well as the STL.

Until then keep Practicing and Stay tuned for more. :)

<img src="https://raw.githubusercontent.com/vedantrathore/vedantrathore.github.io/master/assets/images/keep_calm.jpg" alt="Keep calm and program">

Thanks for being patient and reading..

References:

* <a href="https://www.hackerearth.com/notes/getting-started-with-the-sport-of-programming/">https://www.hackerearth.com/notes/getting-started-with-the-sport-of-programming/</a>
* [https://www.Quora.com](https://www.Quora.com)
* [http://www.geeksforgeeks.org/how-to-begin-with-competitive-programming/](http://www.geeksforgeeks.org/how-to-begin-with-competitive-programming/)
* [https://en.wikipedia.org/wiki/Competitive_programming](https://en.wikipedia.org/wiki/Competitive_programming)

