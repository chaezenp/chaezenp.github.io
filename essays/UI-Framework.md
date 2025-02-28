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
Today, there is a multitude of websites and services that make creating a webpage or website so much easier without touching a single bit of code. Yet sometimes you want the webpage to look a certain way that the program just doesn't allow. So you try to make it yourself. Most webpages are made in HTML, and the basics are simple. Combine it with a little CSS, and your webpage can be as stylish as you want. Then you fall down the rabbit hole of classes, ids, etc, as your code becomes so clustered with `<div class="">` this and `<div id="" class=""> that. You then question whether adding that little bit of flare was worth it. This is where UI frameworks come in. 

# BootStrap not Boot Camp


<div class="container">
  <div class="row justify-content-center">
    <div class="col d-flex flex-column align-items-center">
    <img width="200px" class="rounded" src="../img/UI-reflect/kurzgesagt-home-port.png">
      <h6 class="mt-2">Original</h6>
    </div>
    <div class="col d-flex flex-column align-items-center">
    <img width="200px" class="rounded" src="../img/UI-reflect/my-kurzgesagt-home-port.png">
      <h6 class="mt-2 text-align-left">Remake</h6>
    </div>
  </div>
</div>


I used the UI framework Bootstrap to recreate the Kurzgesagt homepage. I also used Bootstrap to make this side-by-side comparison. The code for the comparison is quite simple.

```
<div class="container">
  <div class="row justify-content-center">
    <div class="col d-flex flex-column align-items-center">
    <img width="200px" class="rounded" src="../img/UI-reflect/kurzgesagt-home-port.png">
      <h6 class="mt-2">Original</h6>
    </div>
    <div class="col d-flex flex-column align-items-center">
    <img width="200px" class="rounded" src="../img/UI-reflect/my-kurzgesagt-home-port.png">
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
```

Like many people, I don't want to waste my time working on something that can be done more efficiently. 

<ul>Grammarly is used to assist in writing this essay only in word choice, spelling, and grammar.</ul>
