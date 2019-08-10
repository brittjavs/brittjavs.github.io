---
layout: post
title:      "RUBY CLI DATA GEM PROJECT"
date:       2019-08-10 19:46:07 +0000
permalink:  ruby_cli_data_gem_project
---


I just completed my CLI Data Gem Project, my first project since I began learning to code. It was an intense two weeks of working on this project. In the process I experienced lots of doubt, and feelings of defeat. But, when I got my code to do what I wanted it to do, I felt extreme joy and satisfaction. This project required a lot of review of what I had learn the previous months. I went through previous labs, watched hours and hours of Avi's resource videos, googled lots, and asked for help when I needed it. Now, I have a CLI based gem that scrapes data, recieves input from a user, and puts out informations according to that input. 

It took me a day or two just to figure out how to create my gem repository and to use github and its commands.
Fortunately, bundler gives you a great file structure to start with. I just had to add the files I knew I would need to my lib folder and get them all connected by requiring them in an environment file. 
```
require_relative './dessert_recipes/scraper'
require_relative './dessert_recipes/cli'
require_relative './dessert_recipes/version'
require_relative './dessert_recipes/recipes'
```

I also had to update gemspec file to add dependencies such and nokogiri, which is our html scraper.

After, that the next step is to find a website to scrape. I wanted to scrape a site I use frequently, so I originally tried scraping websites that had dog-friendly hiking trails. I soon realized that many websites do not have css selectors with any ID or Class labels to differentiate them. This isn't very helpful when trying to scrape large amounts of data. A few days later and zero progress, I decided to change sites. 

One of my joys in life is cooking and baking, so I ended up choosing a Recipe blog to scrape. 
First I scraped the recipe names and url for each recipe. From this data, I initialize recipes and save them to my Recipes class. Second, I scrape each recipe's website to collect ingredients, instructions, serving size, and cooking time. This is where I ran into the most issues. 
1) Because I initialized recipes upon scraping, calling my recipe class, Recipe.all, would come up as nil. I didn't realize until later that I would have to call the scraping class method that instantiated the recipe before I could access Recipe.all.
2) I had trouble figuring out how to collect each ingredient and each step in the instructions, as arrays of individual elements instead of an array with one jumbled string. I tried so many iteration combos but ultimately had to use map method shorthand to achieve this. 
3) My other big issue was that not every recipe had information for serving size and cooking time. I had to add if/esle statements to my scrape so that the information would default to "not available" if the the information was nil. 
```
if page.css("time[itemprop=totalTime]").text != ""
      recipe.total_time = page.css("time[itemprop=totalTime]").text
    else
      recipe.total_time = "Not Available"
    end
```

Once I had all my scraping done I built the controller file for my CLI. Here is where I display recipe names and ask the user to choose a recipe they would like to view by selecting a number. From that input, the terminal will then display all the recipe info from the second scrape for that specific item.

I learned a lot during this project. I found it challenging but now that I have completed it, I am already thinking about improvements and making it more complex. Onward and upward!



