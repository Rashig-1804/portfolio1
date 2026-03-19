---
layout: post
title: Engineering Progress
permalink: /finalportfolio/engineering
codemirror: True
comments: True
microblog: True
---

## #2. <font color="red"> Object Oriented Programming </font>

### <font color="yellow"> Table of Contents </font>
* [Inheritance](#inheritance)
* [OOP Hierarchy](#oop-hierarchy)
* [Object Literals](#object-literals)
* [State Management](#state-management)
* [API Integration](#api-integration)

---


In the development of the **Red Riding Hood**, I used an object-oriented approach. By using classes and inheritance, we created a game where every element, including the **Player** and **Wolf**, behaves as an independent object with its own properties and methods. 

<br>

<a id="inheritance"></a>

### <font color="blue"> Inheritance </font> 

The core of our games is built on inheritance. Instead of rewriting movement, we learned specific characters can "inherit" traits from a base class.

**Example:** In Level 2 of Red Riding Hood, the **Wolf** class uses the **extends** keyword to **inherit** from the **Character** base class


<div class="oop">
  <img src="{{site.baseurl}}/images/oop.png" alt="Image 8" style="border: 2px solid white; width: 50%;">
  <img src="{{site.baseurl}}/images/oop1.png" alt="Image 8" style="border: 2px solid white; width: 50%;">

</div>
<br>

<a id="oop-hierarchy"></a>

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

<br>

<a id="object-literals"></a>

### <font color="blue"> Object Literals </font> 
We avoided "hard-coding" numbers directly into our movement logic, and aimed for **data driven design**. We used **Object Literals** to store sprite data, speeds, and image paths.

**Example**: Our sprite_data_red object stores the height (192) and width (144) of the character. If we want to change the character's size, we **only** have to change it in **one** place, and the rest of the game updates automatically.

<br>

<a id="state-management"></a>

### <font color="blue"> State Management and Collision </font> 
**State Management** occurs to track what is happening in the game. When red riding hood collects 5 cookies, the **"state"** changes to show the congrats popup <br>


<div class="state">
  <img src="{{site.baseurl}}/images/state.png" alt="Image 8" style="border: 2px solid white; width: 50%;">

</div>
<br>

<a id="api-integration"></a>

### <font color="blue"> API Integration </font> 
To manage the transition between levels, I used **API-style calls** to the game engine. By using the `transitionToLevel()` function, Level 1 "talks" to the backend controller to stop the current loop and fetch the data for Level 2. This ensures a smooth flow between different parts of the software.
