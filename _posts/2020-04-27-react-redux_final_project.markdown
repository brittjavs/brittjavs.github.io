---
layout: post
title:      "React-Redux Final Project"
date:       2020-04-28 02:42:13 +0000
permalink:  react-redux_final_project
---


Whoa. I can't believe I made it to the final project. I was really nervous going into it since I had trouble during the redux cirriculum, and rightly so since I ran into quite a bit of trouble along the way. 
For my project I decided to create a plant swapping app called Garden Exchange. It seemed like a simple enough idea. It would have simple transactions between two user. I started planning right away. I wrote out the user story and came up with the following. User should be able to 
1. See all plants available for trade
2. Send an offer for an available plant
3. Post plants up for trade
4. See their own plant listings separate from the feed
5. See offers they have received and sent
6. Accept/Deny offers
7. Search for items through a search bar

I started to write out my models. I was going to need User, Listing, and Offer models. I quickly realized I was going to need login and sessions to keep track of who was logged in order to display user specific listings and offers. This means I would need Sessions model as well. 
In regards to offers, the model was going to need 2 user_ids as well as a listing_id. This was a big hurdle for me. I scoured the interned before I found an article on Stack Overflow that was clear and concise. below is what I needed to add to my Offer migration. 
```
   add_foreign_key :offers, :users, column: :sender_id, primary_key: :id
    add_foreign_key :offers, :users, column: :recipient_id, primary_key: :id
```
```
      t.references :sender
      t.references :recipient
```
I also added the below to my offers model and user models respectively
```
  belongs_to :sender, :class_name => 'User'
    belongs_to :recipient, :class_name => 'User'
```

```
  has_many :sent_offers, :class_name => 'Offer', :foreign_key => 'sender_id'
    has_many :received_offers, :class_name => 'Offer', :foreign_key => 'recipient_id'
```

Being able to pass three id's from the frontend was also tricky. I ended up creating offers through current_user so it would be associated with the sender_id on creation. I sent the listing_id from the front end and after creation but before save, I assigned the listing.user_id as the recipient_id. 


Setting up the frontend I ran into some issues with the middleware and the redux devtools extension. It didn't work the way we were shown to set it up in the cirriculum. I had to create a composeEnhancers variable that was equal to the redux extension or compose. I called this in the store with applyMiddleware(thunk) as an argument to composeEnhancers. 

About a week in to the project I got completely stuck when creating listings. It was not registering a current_user in my listings controller but it was registering in my offers controller. After asking for help and opinions, I decided to start over and test every single action along the way to make sure a user was logged in and there was a current_user in the backend. It was a great delay but it worked the second time around. 

There were many other difficulties including learning to create a searchbar, figuring out how to fetch data for all the components without having duplicate objects in the store. 

This project was an extreme challenge for me. I learned so much and am now heaps more comfortable working with the redux store, mapStateToProps and mapDispatchToProps. 
