---
layout: essay
type: essay
title: "Patterns for the masses"
# All dates must be YYYY-MM-DD format!
date: 2025-04-24
published: true
labels:
  - Design Patterns
  - Programming
---

<img width="20%" class="rounded float-start pe-4" src="https://cdn.pixabay.com/photo/2020/05/30/17/57/flower-5239814_1280.jpg">


# A Common Solution
As the years go by, people will continue to arrive at problems that block their path. But if you're lucky, someone out in the world has come to this problem before (and hopefully found a solution). Especially nowadays with the internet, these solutions from the past are archived and much more accessible. And sometimes you may have a semi-specific problem, but you still manage to find a solution while not exact still works. In software development, more often than not, people will face problems with code. This can be remedied with Design Patterns, which are general, well-tested solutions to common problems many face in software development. They serve as blueprints to create reusable and maintainable code. Using design patterns allows developers to work more efficiently, as they don't have to reinvent the wheel, while allowing flexibility to modify if needed. Using design patterns is very useful in a team setting. It can effectively communicate how you wrote a piece of software while not explicitly stating it. 


# Patterns Are Useful
Design patterns come in three types: Creational, Structural, and Behavioral.
Creational: Focuses on the process or challenges of object creation and how to instantiate objects flexibly and efficiently.
Structural: Focuses on the organization and composition of classes and objects to create larger structures while ensuring flexibility and scalability.
Behavioral: Focuses on the communication and interaction between objects, managing how they collaborate and share responsibilities.
The best way to demonstrate how useful design patterns are is to use examples.

When developing [Harmony Quest](https://chaezenp.github.io/projects/harmonyquest.html) and [The Night March](https://chaezenp.github.io/projects/night-march.html) I used at least one of each type of design patterns. 

When creating levels with dynamic platforms, such as a moving platform, it would be very inefficient to recreate it in each level. As I developed these two games in **Unity**, I was able to make a ``prefab``, a reusable game object or asset that can be easily instantiated or modified across multiple levels, containing premade settings, components, and behaviors. In Harmony Quest, I used many ``prefabs`` for platforms and player types to be easily implemented into any level. This is an example of a **Prototype Design Pattern**, a Creational Design Pattern, in which you save an existing object, which would otherwise be time-consuming to re-create, and copy/clone it. 

Something everyone is familiar with is a menu system, whether it be in Google Drive or a music app. As in many games, I also developed a simple menu system with sub-menus for sound settings, a controls page, and credits to my team. This is an example of a **Composite Design Pattern**, a Structural Design Pattern, that allows you to treat individual objects and groups of objects uniformly, typically by organizing objects into tree-like structures. 

I often used the state of the player character to determine what they can and can't do. For example, to negate an infinite jump, I would check to determine if the player was on the ground, like:
```
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float jumpForce = 10f; // Adjust the jump force to your liking
    private bool isGrounded; // To check if the player is on the ground
    private Rigidbody2D rb; // Reference to the Rigidbody2D component

    void Start()
    {
        rb = GetComponent<Rigidbody2D>(); // Get the Rigidbody2D component
    }

    void Update()
    {
        CheckGrounded(); // Check if the player is on the ground
        
        if (isGrounded && Input.GetButtonDown("Jump")) // If player is on the ground and presses jump button
        {
            Jump();
        }
    }

    void CheckGrounded()
    {
        // Raycast or collision check to see if the player is on the ground
        isGrounded = Physics2D.Raycast(transform.position, Vector2.down, 0.1f); // Simple raycast downward from the player
    }

    void Jump()
    {
        rb.velocity = new Vector2(rb.velocity.x, jumpForce); // Apply the jump force on the y-axis
    }
}
```


This is an example of **State Design Pattern**, a Behavioral type of Design Pattern, in which it changes the behavior based on an object's state. In this case, the player is in the air, therefore, you can't jump again until contact with the ground or a ground-type platform. This can be applied to a multitude of states the player may be in, like mud, slowing a player's movement down, or a player being able to jump higher in a "low-gravity" zone. 
