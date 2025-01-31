---
layout: essay
type: essay
title: "A 'Smart' Question"
# All dates must be YYYY-MM-DD format!
date: 2025-01-30
published: true
labels:
  - Software Engineering
  - Learning
  - Community
---

<img width="250px" class="rounded float-start pe-4" src="../img/reflec-smartQs/stackOverflow_essayPic.png">


# How can a question be 'smart'?
When you ask a question, the person you're asking may or may not have an answer. If they happen to have an answer, it may not be the one you're looking for. There are many reasons why that may be, but you have to ask another question. One to yourself, "Was it a **smart** question?". Yes, there is "no such thing as a *dumb* question" but, like baking, you need details, you need measurements. This is especially true in software engineering. A vague question may get you an acceptable answer but more often than not, you won't. That is why an educated smart question must be asked. 

At its core, a smart question stems from a good sense of communication. Can you clearly and specifically ask the question? Get your point across effectively? You can't get help if you don't communicate it properly. In the realm of programming and software engineering, problems can be very technical, so you must be detailed in your questions. And in this case, the internet is your friend. There were many times when a simple Google search found the exact solution that I needed. Other times the solutions were similar but needed some adjustments. Then sometimes none at all. But that is why you research first to not be redundant. Then along with your question, you talk about what you've tried, found success in, and where you got stuck. This will give everyone who comes across the question the tools necessary to help you. 

Here is an example from [Stack Overflow](https://stackoverflow.com/questions/79347608/why-does-a-a-x-i-i-and-a-x-i-i-return-two-different-results) about how computers interpret arithmetic.  
```
Q: Why does a = a * (x + i) / i; and a *= (x + i) / i; return two different results?

With the text included:
I am calculating the number of routes possible in a 20 * 20 grid from top left to bottom right when only down and right moves are possible.

I read about calculating the central binomial coefficient to calculate the routes and implemented it in my code:

And then provides code of two methods with the second containing:
    for (int i = 1; i <= x; i++)
    {
        result = result * (x + i) / i;
    }
```
The Orignal Poster (OP) provided a link to an article (central binomial coefficient) about what they're trying to accomplish and continues about how `result = result * (x + i) / i;` works but not `result *= (x + i) / i;` and is trying to understand the difference. 

The person who answered starts with two links about `operator precedence` and `integer division`:
```
A: It is a matter of operator precedence together with the nature of integer division.

*= has lower precedence than normal arithmetic operators (+,-,*,/).

And explains how:
result *= (x + i) / i; is equivalent to result = result * ((x + i) / i);
and 
result = result * (x + i) / i; is equivalent to result = (result * (x + i)) / i;

```
h
