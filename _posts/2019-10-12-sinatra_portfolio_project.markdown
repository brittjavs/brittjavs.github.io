---
layout: post
title:      "Sinatra Portfolio Project"
date:       2019-10-12 17:51:42 -0400
permalink:  sinatra_portfolio_project
---

For this project I chose to make an app that I would find useful in my own life. I love to camp but after a few months, I forget details like dates, and campground names of places I have camped so I wanted a way to keep track them as well as to have a Bucket List of places I would like to camp at. So, I created an app called CampTales which is a camping journal that allows campers like me to sign up for a journal account where they can create and edit entries to both journal and bucket list. It was a fun process and I felt more comfortable creating from scratch compared to the CLI project. 

The first step I took in the process of building this app was to create an excel sheet that would help me map the MVC and CRUD actions. I started with a column for each of my models, camper & trips. I listed what each would have in their databases such as username, password for camper and park and campground for trips. I would need a controller for each model which is what I listed next. I thought about what routes each controller would need and listed them out along with routes or forms they would redirect to. From there I knew what forms and other view files I would need. 

![](https://lh6.googleusercontent.com/9EV-3oZHu5JjRGw9Ozi2mwxK-e3kIGW35gb9RfKNngKOic3vb76eECoCDSA=w2400)

This excel sheet was super helpful. I created my repo in github and used the corneal gem for prebuilt file structure. I started coding everything I listed out so I had the basic app structure coded fairly quickly. From there I created a seed file I'd be able to use for testing. There are a few ways to do this and wasn't sure about the best way to go abot it but I ended up using the create method like below.

```
Camper.create(email: 'billie@cutepups.com', password: 'yummytreats', username: 'BillieThePup')
```

Once I had all my view files I started testing. I have grown to enjoy testing and breaking the app. The problem solving and debugging is my favorite part. I began adding more logic and reroutes as well as validations in my models. 

The final part of the project is making it look nicer. I come from a graphic design background so I know it would be all too easy for me to become fixated and obessed with making it look a certain way. Because of this, and my minimal CSS skills i decided to keep it simple, look through templates, find one I liked, and apply it to my own application. 

This was a fun project and I was able to keep my cool, plan, and execute. Onward and upward!

