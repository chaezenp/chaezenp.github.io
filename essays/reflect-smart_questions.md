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
When you ask a question, the person you're asking may or may not have an answer. If they happen to have an answer, it may not be the one you're looking for. There are many reasons why that may be, but you have to ask another question. One to yourself, "Was it a **smart** question?". Yes, there is "no such thing as a *dumb* question," but, like baking, you need details, you need measurements. This is especially true in software engineering. A vague question may get you an acceptable answer, but more often than not, you won't. That is why an educated, smart question must be asked. 

At its core, a smart question stems from a good sense of communication. Can you clearly and specifically ask the question? Get your point across effectively? You can't get help if you don't communicate it properly. In the realm of programming and software engineering, problems can be very technical, so you must be detailed in your questions. And in this case, the internet is your friend. There were many times when a simple Google search found the exact solution that I needed. Other times, the solutions were similar but needed some adjustments. Then sometimes none at all. But that is why you research first, so as to not be redundant. Then along with your question, you talk about what you've tried, found success in, and where you got stuck. This will give everyone who comes across the question the tools necessary to help you. 

# A Smart Question
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
result = result * (x + i) / i; is equivalent to result = (result * (x + i)) / I;

Then an example with numbers. 

```
The Answer Poster (AP) has a few edits with a *Note* section referencing the comments on their answer which explains why 
`result * (x + i) will always be divisible by i` and the mathematical proof of the expression. Ending with a *final note* about a rule of thumb for multiplying before dividing to decrease error in integer division in most cases. 

# Why is it Smart?

**Specific**: The question is very specific, addressing one line of code and showing that OP wants to understand why one works but not the other. 

**Context and Effort**: OP provides a link to an article about what they are trying to accomplish and how it gave them one answer but not the other.

**Focus**: OP only focuses on the one line of arithmetic that they don't understand.

This is a great example of a 'smart' question as it leads to a clear and concise answer from AP and the commenters, with the bonus of a 'rule of thumb' to reduce the amount of errors similar to integer division (though being case by case). Since this was on Stack Overflow, it is public and open to anyone to find if they have the same question. 

# A (not) Smart Question
An example of a [not Smart Question](https://stackoverflow.com/questions/79256830/error-in-creating-new-react-app-using-create-react-app-appname) is:
```
Q: Error in creating new React app using create-react-app appname

Followed by copy and pasted errors:

npm error code ERESOLVE
npm error ERESOLVE unable to resolve dependency tree
etc....
```
There are a few different answers but none have been accepted by the OP. Some considered switching to another build tool and two had the same answer. The first comment on the original question ends with "provide more details", which is a clear sign that OP did not ask a smart  question.

# Why is it not Smart?
**Vague**: OP did not provide any specific details on their problem and only posted their error code.

**No Effort**: OP did not show any effort to try and solve their problem before posting.

# Conclusion: Be Smart, Ask Smart
Asking smart questions is better for the one asking and anyone who is trying to answer. When you are clear and specific, and provide context about what you’re trying to do, the person who answers can be as clear and precise while offering bonus tips and advice. That way, both sides can save time and work more efficiently to solve problems and learn. “There are no dumb questions,” but there is a smarter way to ask them.
