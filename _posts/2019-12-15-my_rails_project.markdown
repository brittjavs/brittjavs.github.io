---
layout: post
title:      "My Rails Project"
date:       2019-12-15 01:37:59 -0500
permalink:  my_rails_project
---


This project has been the toughest one yet. I think there was so much to learn in the Rails module that it was a bit more difficult to retain all the information and lessons compared to the last few modules. That being said, I do feel like I have come a long way but I am aware I still need more practice.

For my project, I created an application I called Dear Creatures. It is a charity app that allows a user to create an account, browse through some animal shelters and rescues, and donate items or monetary gifts.

Originally I wanted to use only 3 models in this project, one for Users, one for Shelters, and a join model for Donations. I ended up using 5 models with 2 many-to-many relationships (Users have many Shelters through Donations  - Shelters have many Users through Donations , and Shelters have many Items through NeededItems - Items have many Shelters through NeededItems. It took a while to figure out the associations but eventually it made sense.

The most difficult part of this project for me was getting quantities and amounts to update once a User submitted the Donation form. Both Donation and NeededItems tables have qty and dollar_amount fields to make this action possible. I knew I was going to need a method that would subtract the donated amount/qty from the NeededItem qty/amount. It took me a while to figure out where the method would go. Eventually I figured out this would go in the model that was being updated, NeededItems. It needed arguments that would be passed from the Donation model inorder to find the correct record to update in the database. I also learned that params from the form are strings so they needed to be converted into integers. 
Below is the class method i used to update qty.

![](https://lh5.googleusercontent.com/Qlda91ELpBOyqdYtLHU1YYmCl8B4-grfhYdh_Cb7TVCjMCutVdaFEBgomSM=w900)



A few other firsts for me included the use of scope and third-party login using omniauth. 
I am looking forward to adding more features to this project once I have more practice in Rails and learn Javascript. 
Onward and Upward! 

