---
layout: essay
type: essay
title: "Going Beyond Engineering Software"
# All dates must be YYYY-MM-DD format!
date: 2025-05-14
published: true
labels:
  - Software Engineering
  - Coding Standards
  - Design Patterns
  - Functional Programming
---

<img width="50%" class="rounded float-start pe-4" src="../img/reflectSE/CodingComputer.jpg">


Throughout my software engineering course, I have gained much more knowledge about programming concepts, methods, and other tools to help development. While most assignments focused on web development, the core of this class was to *think* like a software engineer, to use what we have learned on future projects beyond web applications and front-end development. I have gained a greater appreciation for the **standards I hold for myself in my work, the patterns I can utilize to develop more efficiently, and functional programming to expedite my development.**

# Structure: Coding Standards
When I first started this class, my code documentation was standard. I commented on the main aspects of the code, only going into detail about functions that were not intuitive. I just commented enough to get a good grade, with a previous class that required comments couldn't be more than 80 characters long (indentation included). Now that I have used ``ESLint``, a code analysis tool for JavaScript, and its extension ``Prettier ESLint`` (more formatting) as the coding standard in my software engineering course, I see how much it has made my code visually appealing and error-free. ESLint is also a great tool for learning JavaScript and TypeScript syntax, as it catches all types of errors. And with ``Prettier`` in your integrated development environment (IDE), you can have it automatically format your code as you write to save the hassle at the end. 

Using this coding standard has shown me how important having a structure is. Not only does it result in having clean code, but it also results in having code that is easier to debug, maintain, and update, especially by others. Having this structure leads to others understanding it better. The formatting, naming conventions, and consistent logic can be shared throughout a project, leading to an efficient workflow among teams in which reduces the misunderstandings and errors that could have happened previously. It's also good practice for future developers who need to update or modify the program. 

Having a defined structure for a collaborative setting is a must to keep everything organized and well-maintained. Using and maintaining a consistent structure reinforces the habit of noticing inconsistencies while writing code, and it forces you into a discipline that will help you be more focused, consistent, and organized. 


# Blueprints: Design Patterns
As coding standards are used to reduce headaches in the format and readability of the code, design patterns are used to reduce headaches in defining and solving problems. Design patterns are general, well-tested solutions to common problems many face in software development. It's not the direct solution, but it provides the blueprints to start building one and is not tied to any specific coding language or application.

While building [Manoa Connect](https://chaezenp.github.io/projects/Manoa-Connect.html), we utilized the **Builder Pattern** for account creation and modification as the profiles all have unique information but still share the same components. Then I used **State Pattern** for determining whether another user should be presented on the connect page, in other words, if you have already matched or liked a profile, it won't show up in the connect page again. 
<img width="50%" class="rounded float-end pe-4" src="../img/ManoaConnect/MC-ConnectPage.png">


Just like using a coding standard, applying a design pattern provides structure and keeps everyone on the team on the same page. It sets up expectations of how the component of the project should behave. Using these patterns isn't just for web development, but can be used for a multitude of systems, like in game development (which I have), desktop applications, or robotics software. 

I think the concept of design patterns is very powerful as it can be used in a wide variety of professions. It promotes a method of problem-solving that uses solutions that can be reused and repurposed to fit the challenge at hand. It guides decision making, can streamline efforts, and promotes modular thinking. Design patterns is a useful tool for creating flexible approaches to problems without having to reinvent the wheel. 


# Action: Functional Programming

The core idea of functional Programming (FP) is writing pure functions with no side effects, ensuring consistent and predictable behavior. When I first learned about this concept, it was confusing. But as the class went on, I developed my skills in JavaScript/TypeScript, which worked in tandem with functional programming. It has become a handy tool when implementing functions, as I can design them to be versatile. It helped when developing [Manoa Connect](https://chaezenp.github.io/projects/Manoa-Connect.html) as it kept code concise and modular. 

An example of functional programming from Manoa Connect is a function I made to create an expandable list based on a string that is divided by commas, such as a user's class list

```
const ClassList = ({ label, classListString, previewCount = 3 }: ClassListProps) => {
  const [isExpanded, setIsExpanded] = useState(false);

  const classList = classListString
    ? classListString.split(',').map((item) => item.trim())
    : [];

  const visibleList = isExpanded ? classList : classList.slice(0, previewCount);
  const hasMore = classList.length > previewCount;
...
```
The naming convention could have been broader, but the scope was for a list of classes. The code above can be used for any list in a string input.

Functional programming is meant to be reusable for many applications. What I've learned is not to repeat myself when I can avoid it. I aim to find general and adaptable methods to achieve my goals, not just in web development, but with programming as a whole. For example, when developing [Harmony Quest](https://chaezenp.github.io/projects/harmonyquest.html), I relied on the use of prefabs: a reusable game object or asset that can be easily instantiated. Instead of recreating a player or platform object each time, prefabs allowed me to build them once and reuse them as needed. This matches the core idea of functional programming — promoting a mindset of clear, consistent, and scalable problem-solving. By creating stable and reusable solutions, I can save time, reduce the complexity, and set up systems that can adapt to future needs.

# Conclusion
In the time I spent in my software engineering course, coding standards, design patterns, and functional programming aren't just technical tools — they represent disciplined ways of thinking. These principles emphasize clarity, consistency, reusability, and efficiency, which can be applied to many aspects of programming beyond software engineering. It leads to maintainable and scalable code in general and can be used for problem-solving outside of coding. It encourages adaptability and thoughtful design. Whether you're writing a function, working in a team, or solving real-world challenges, these fundamental principles help cultivate a mindset focused on solving the right problems most effectively and efficiently possible.

``Used Grammarly and ChatGPT for word choice and to improve clarity and flow.``
