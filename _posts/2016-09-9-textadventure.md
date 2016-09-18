---
layout: posts
title: Text Adventures in Python
---

<article>
<h1>Text Adventures in Python</h1>

<p>Over the last week at bootcamp, we have dived deep into OOP in Python.
The mission was to design and create a text-based adventure game. After considering many
game concepts, my game theme was chosen and some basic planning began.</p>

<p>The most important lesson I have learned about the object oriented approach to programming
anything is that planning, organization, and prioritizing small tasks are critical steps.
While project planning and management are key steps to designing and building anything,
I realized that planning is a skill. Like all skills, they take regular practice to improve upon.</p>

<p>In the past, the extent of project planning I've done on my own small projects has
been rather limited. I am in the habit of putting a lot of implementation notes in a README document -
and calling it good. Planning should be a simple process that uses simple tools, but one document and
perhaps a Wiki may not be the best place to isolate small tasks and goals.</p>

<p>From now on, I'll be using a small set of dedicated tools for organization and planning.
I will keep the content of README and Wiki documents aimed toward users, while using Github issues
for specific implementation tasks and project milestones.</p>

<p>With planning and project setup complete, on to thoughts on object oriented programming.
I decided make a ninja game. The requirements were to have a character who could move through
rooms or stages, battle enemies or complete some task, and have some notion
of an inventory.</p>

<p>I limited the game environment to a 3 x 3 grid representing city blocks. Implementing the movement
of the ninja from one block to the next was a rewarding experience. Especially, figuring out the logic
to give the city (a Python list of 9 objects) boundaries that the player cannot move past. Below, I've included a little about the classes and methods I used. I will be writing another blog post that will detail how to define edges of a square grid, or matrix for representing a map.</p>

<h3>I am an object. What do I need to know about? What do I need to do?</h3>

<p>I learned this (above) is a very helpful approach to designing a Class and it's corresponding methods. I have the following classes in my game:</p>

<ul>
  <li>Game - The game class contains instances of game objects and control flow methods.</li>
  <li>Ninja - The main player character.</li>
  <li>Badguy - The game environment has 5 instances of badguy.</li>
  <li>Building - 1 building instance per city block.</li>
  <li>City - The city has a single `blocks` attribute, a list containing 9 instances of Building.</li>
</ul>

<p>Okay, simple right? That's what I thought until I had those class definitions in one file, along with many
other helper functions and all the string constants for the game. At over 700 LOC, it quickly became hard to debug,
extend, and even explain. I planned to modularize the classes into their own files once I had the basic features working,
but it became increasingly difficult to split up the functionality. More so, the game worked and was playable!
So, I feared breaking it in order to properly refactor the many nooks and crannies within the massive 1 file game.
</p>

<p>Once I dove in and started placing each class definition in it's own file, I noticed other areas that could be separated as well.
It took a few frustrating hours to get the game back running. Once the dust cleared, it was a huge relief. It was a very rewarding
experience to modularize my game into many files, and I learned (the hard way) to never start a project as one large file again.</p>

</article>