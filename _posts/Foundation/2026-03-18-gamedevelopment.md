---
layout: post
title: Rashi's Game Development Progress!
permalink: /finalportfolio/gamedevelopment
codemirror: True
comments: True
microblog: True
---

### <font color="yellow"> Table of Contents </font>
* [Custom Level Testing](#testing)
* [NPC AI](#npc)
* [Incorporation of 5+ Methods](#methods)

<a id="testing"></a>

### <font color="blue"> Custom Level Testing </font>

The Red Riding Hood game is a fully playable experience designed for the team repository: new_csse2_team. We created a progression system where the player, **Red Riding** must complete a collection task in **Level 1** before moving to the survival-based **Level 2**. 
<br>

We tested the transition logic to ensure that assets like the "Congrats" popup and the "Level Title" are properly created and then removed using a **</font color="red"> destroy() </font>** method. 

<div class="img2">
  <img src="{{site.baseurl}}/images/testing.png" alt="Image 8" style="border: 2px solid white; width: 60%;">
</div>


<a id="npc"></a>

### <font color="blue"> NPC AI </font>
The **Wolf** in Level 2 features a custom AI pathing system. Instead of moving randomly, it follows a set of **Waypoints** stored in an array.

<div class="img3">
  <img src="{{site.baseurl}}/images/npc_ai.png" alt="Image 9" style="border: 2px solid white; width: 60%;">
</div>


<a id="methods"></a>
<br>

### <font color="blue"> Incorporation of 5+ Methods </font>

I utilized complex methods throughout the game that process information and return specific results.

1. checkCollision(player, cookie)

2. checkInZone(player, zone)

3. buildWayPoints()

4. draw(debug)

5. checkPlayerWolfCollision(player, wolf)


<div class="img4">
  <img src="{{site.baseurl}}/images/check_collision.png" alt="Image 9" style="border: 2px solid white; width: 60%;">

  <br>
  <br>
  <img src="{{site.baseurl}}/images/zone.png" alt="Image 9" style="border: 2px solid white; width: 60%;">

  <br>
  <br>
  <img src="{{site.baseurl}}/images/draw_debug.png" alt="Image 9" style="border: 2px solid white; width: 60%;">

  <br>
  <br>
  <img src="{{site.baseurl}}/images/wolf_collision.png" alt="Image 9" style="border: 2px solid white; width: 60%;">

</div>



