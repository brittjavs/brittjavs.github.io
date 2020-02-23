---
layout: post
title:      "Rails JS Project"
date:       2020-02-23 04:52:16 +0000
permalink:  rails_js_project
---


This project requred a signle page application built with a rails api with javascript frontend. This project was very different from the past projects for various reasons; reasons that made this project extra challenging. I will be writing about my experience.

1. Before I started writing any code, I brainstormed and decided what i wanted my applicaton to be. I wanted to create something space related, and personally I love stargazing so I decided to create a tracker for constellations. 
2.  I wrote user stories. This outlined what i wanted the user experience to be like. For example,
     * User can view all constellations.
     * User can contribute observations.
     * User can keep track of their observations while still viewing all the constellations.
3.  I drew out what I wanted the page to look like. I wanted a card for each constellation that would display the image and name of constellation along with buttons to add an observation.
4.  Then I decided to list out what I would need in the api. Models, classes (User, observations, Constellations), attributes for each model(:name, :location, :clarity, etc).

After all the planning I felt ready to start writing code. The file structure was fairly new to me and took me a bit to wrap my head around it. Once I got that set up I began creating my backend files. We are supposed to work vertically, meaning not building out all models, then all controllers, but instead each feature at a time. I started with the constellations which was going well until I needed to start adding in observation features.  I also realized I had no clue how to implement users and have their observations be emphasized on the page with all constellations. Due to time restraints I had to scrap the User.

Throughout the whole project I ran into a lot of issues because of how I had designed my page. I wanted each card to have its own functioning buttons that would toggle information. This made my frontend code very complicated and to be honest, kind of ugly and perhaps not so RESTful. My JS Constellation class became my page manager. I had to create everything in this class since all my cards would need to hold their own observation list, and their own form. The form to create an observation was within my constellation card so I couldn't use the ObservationAdapter to make my fetch call to post a new observation. Since I was rendering everything after fetching the constellation json, I created most elements in my render function. This made querying elements, and having event listeners outside of this function extremely complicated. 

Most of my planning went out the window. While the end result is still similar to my original idea, I had to make changes and adapt as I got further along in my code. Now that I my project is complete I am reflecting on form vs function as it applies to code. I am also thinking about how in code, like life, no matter how much you plan and prepare, things will not always go as planned and you will have to adapt and just keep going. I definetely want to take more time to refactor and clean up my code as well as add in another feature or two such as editing observations as well as possibly adding user models/classes. 
  
