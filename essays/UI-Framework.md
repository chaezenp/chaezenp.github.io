---
layout: essay
type: essay
title: "Intricacies of a webpage"
date: 2025-02-27
published: true
labels:
  - HTML
  - BootStrap
  - UI
---

# Webpages, Webpages...
Today, there is a multitude of websites and services that make creating a webpage or website so much easier without touching a single bit of code. Yet sometimes you want the webpage to look a certain way that the program just doesn't allow. So you try to make it yourself. Most webpages are made in HTML, and the basics are simple. Combine it with a little CSS, and your webpage can be as stylish as you want. Then you fall down the rabbit hole of classes, ids, etc, as your code becomes so clustered with `<div class="">` this and `<div id="" class="">` that. You then question whether adding that little bit of flare was worth it. This is where UI frameworks come in. 

<div class="container">
  <div class="row">
<img width="250px" class="rounded float-start pe-4" src="../img/UI-reflect/bootstrap-logo.png">
<h1>not Boot Camp</h1>
</div>
</div>


"Build fast, responsive sites with Bootstrap"


<div class="container">
  <div class="row justify-content-center">
    <div class="col d-flex flex-column align-items-center">
    <img class="img-fluid" src="../img/UI-reflect/kurzgesagt-home-port.png">
      <h6 class="mt-2">Original</h6>
    </div>
    <div class="col d-flex flex-column align-items-center">
    <img class="img-fluid" src="../img/UI-reflect/my-kurzgesagt-home-port.png">
      <h6 class="mt-2 text-align-left">Remake</h6>
    </div>
  </div>
</div>


I used the UI framework Bootstrap 5 to recreate the Kurzgesagt homepage. I also used Bootstrap to make this side-by-side comparison. The code for the comparison is quite simple.

```
<div class="container">
  <div class="row justify-content-center">
    <div class="col d-flex flex-column align-items-center">
    <img class="img-fluid" src="../img/UI-reflect/kurzgesagt-home-port.png">
      <h6 class="mt-2">Original</h6>
    </div>
    <div class="col d-flex flex-column align-items-center">
    <img class="img-fluid" src="../img/UI-reflect/my-kurzgesagt-home-port.png">
      <h6 class="mt-2">Remake</h6>
    </div>
  </div>
</div>
```
Compared to standard HTML, I would have to define each of these classes in a CSS file before implementing them.
```
**CSS File**

.container {
  width: 100%;
  padding: 20px;
  display: flex;
  justify-content: center;
}

.row {
  display: flex;
  justify-content: center;
  gap: 20px;
}

.col {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.image-fluid {
  width: 100%;
  height: auto;
}
```

Like many people, I don't want to waste my time working on something that can be done more efficiently or automatically. Bootstrap 5 is said to be "responsive, mobile-first, and easy to use", giving users a grid system to make aligning things so much easier. 

When I was recreating this homepage, Bootstrap laid the groundwork of the top menu "navbar", the content section, and the footer. But like missing a semicolon in Java, a misplaced or missing `</div>` or other closing tag can throw everything off (most times literally) and end up wasting more time. I wasted a lot of time trying to center and offset the text floating above the middle image, which I decided to just use CSS classes and id's to save the rest of my sanity to build the rest of the page. 

Using Bootstrap is a double-edged sword, as making the "More about us" button was a simple line of code, but it isn't as vibrant and round as the original. And as I said previously, sometimes the grid system doesn't work in your favor. 

# What I learned?
Bootstrap (and other UI frameworks alike) are game-changers for fast web development. But they are there to help you, not do it all for you. You still need to understand HTML and CSS to use these tools successfully. With enough practice, you can create pages that are digital wonders. 

<ul>Grammarly is used to assist in writing this essay only in word choice, spelling, and grammar.</ul>
