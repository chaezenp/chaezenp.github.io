---
layout: essay
type: essay
title: "TypeScript: A New Language"
# All dates must be YYYY-MM-DD format!
date: 2025-01-23
published: true
labels:
  - Software Engineering
  - Learning
  - Javascript/Typescript
---

<img width="150px" class="rounded float-start pe-4" src="../img/reflect-ts/TypeScriptSquare.png">

# Previously...
I have coded in Java for the most part with C# second and C/C++ in third. I am most comfortable with Java as it is the language I've used the most. I have become accustomed to the class declaration and main method of Java:

```
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```
So I may have a bias toward Java, but I am always open to not writing so much syntax to produce a program. However many systems, especially older ones, still use Java and I think it is still a language worth learning and knowing (for now). 

# A New Language
I've heard about Javascript before and how it and Java only share the name but Typescript is something completely new to me. Just learning the basics, I have found Typescript to be very interesting. An interesting part that is different from other languages I have programmed in like Java and C#, is Typescript's functions, variables, and objects can be assigned different types, therefore making the code flexible for different applications. 

Union types are what make this possible. It is quite simple as well, using '|' (pipe):
```
function printFunc(printThis: string | number): string | number {
return printThis;
}
let num: number = 4;
console.log(printFunc("Lol")); // Prints Lol
console.log(printFunc(num)); // Prints 4
```
Also compared to Java, printing to the console is much simpler as all you need is *console.log("Lol");*. But with less syntax one way, there is more the other way. What I mean is Typescript is a superset of Javascript and a main difference is Typescript is about explicit types. Then again some programs run better on Java and some on Typescript, it all depends on the application.

Another thing I find interesting is that **any** and **unknown** in typescript can be dynamically typed like **let** in Javascript. They can change throughout the code which can be useful or hurtful. But to avoid the hurt, it is recommended to use **unknown** as it is safer than **any** so I'll stick with **unknown**.
Though I am still new to this language, I think learning and practicing more will be worth it.

# Going Forward
Like anything you are learning and trying to get comfortable with, practice is the key. Using something like the Workout of the Day (W.O.D), a timed exercise in which you program a solution to a given problem can help me develop my skills in programming in general. As of now, I have done three W.O.Ds and have seen how I tend to find a longer way to the solution. But with practice, I should be able to write more concisely to achieve my goal. 
I will bring this type of learning/practice into new languages that I want to learn such as Python and ones I'm familiar with. 

<ul>Grammarly is used to assist in writing this essay only in word choice, spelling, and grammar.</ul>
