---
layout: post
title:      "Intro to Sinatra"
date:       2019-09-16 00:06:12 +0000
permalink:  intro_to_sinatra
---


This past week I completed Sinatra Basics and learned about MVC. 
Sinatra is considered a lightweight framework because the developer is still responsible for the structure and communication of web applications. You have to manually set up routes and connect them to the rest of the application. 

Sinatra gives us access to methods like GET and POST which are required to set up routes. Routes allow a web application to receive HTTP requests. Below is an example of a route. 

```
get '/hello' do 
		erb :hello
		end
```

Sinatra uses **MVC** model which stands for Model View Controller.
* **Models** are where data is saved and manipulated.
* **Views** contain our HTML and the code for what the User sees and interacts with.
* **Controllers** are our Ruby Classes that contain our routes.
Each part of this model has its own tasks which create separation of concerns.

The route above will connect to a hello.erb file(found in our 'views' folder)as a response if the controller receives an HTTP request(url) for our application ending in '/hello'. The view file with our html would look something like this:
```
<!DOCTYPE html>
<html>
    <head>
        <title>Hello</title>
    </head>
    <body>
        <h1>Hello World</h1>
    </body>
</html>
```

The user would see Hello World on the page.

I am starting to understand the interaction between each section of our MVC model and I am looking forward to building more complex web applications. Onward and upward!

