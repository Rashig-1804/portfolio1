---
layout: post
title: Engineering Progress
permalink: /finalportfolio/engineering
codemirror: True
comments: True
microblog: True
---

## #2. <font color="red"> Object Oriented Programming </font>

In the development of the **Red Riding Hood**, I used an object-oriented approach. By using classes and inheritance, we created a game where every element, including the **Player** and **Wolf**, behaves as an independent object with its own properties and methods. 

<br>

### <font color="blue"> Inheritance </font>

The core of our games is built on inheritance. Instead of rewriting movement, we learned specific characters can "inherit" traits from a base class.

**Example:** In Level 2 of Red Riding Hood, the **Wolf** class uses the **extends** keyword to **inherit** from the **Character** base class


<div class="oop">
  <img src="{{site.baseurl}}/images/oop.png" alt="Image 8" style="border: 2px solid white; width: 50%;">
  <img src="{{site.baseurl}}/images/oop1.png" alt="Image 8" style="border: 2px solid white; width: 50%;">

</div>

### <font color="blue"> OOP Hierarchy </font>
In our **Red Riding Hood** game, we didn't write the same code over and over for every character. Instead, we used a class hierarchy.
<br>

The Parent (Character): This is the "base class" <br>
The Children (Wolf and Player): These are "sub classes"
<br>
<br>

By calling a special function **super()**, the wolf reaches up into the Parent class and grabs all the important foundations like gravity and screen position, so we don't have to code them again.
<br>

<div class="super">
  <img src="{{site.baseurl}}/images/super.png" alt="Image 8" style="border: 2px solid white; width: 50%;">

</div>