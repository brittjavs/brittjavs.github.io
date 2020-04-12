---
layout: post
title:      "Ch-Ch-Changes"
date:       2020-04-12 22:44:14 +0000
permalink:  ch-ch-changes
---

* A lot has changed over the last month. Due to "stay at home" rules, I began working from home which is something I had never done before. Luckily, I am working as graphic designer so all I need is a computer for my job. But it is a brand new work environment and has presented some challenges for me. I have found it a bit more difficult to focus on my work for long periods of time. My most productive hours are now early in the morning before my housemates crowd my workspace and in the night time when everyone is in their own quarters. 
* In normal times, I feel like I have time to decompress from my work day on my drive home and prepare myself mentally to come home and work on Flatiron coursework. There is a separation in my day that I miss but have done my best to recreate this. I have one area where I have my iMac set up just for my 8-5 work. Once my work day is over, I take my dog out to the yard to play, have dinner, watch jeopardy, and then start my coursework. It took a couple of weeks to get into this new routine but I finally feel better about it. 
* During this time in my cohort, we learned React and Redux. I was really enjoying React because of the potential of funcitonality and improvement in the users experience. It also gives us the ability to pass props from one component to another which was something that was very frustrating when we were coding with vanilla JavaScript. But, once we got to Redux, I felt so lost. Everything seemed jumbled to me and I didn't know what component was responsible for what or where props were coming from. It wasn't until this past week that I had a breakthrough. I had a really helpful pair programming session with a fellow student who went through a full lab with me. Now I can share a few things I have learned in regards to Redux.
1. We use createStore() to return a store that has functions to get and dispatch state and props. This is usually done in index.js. 
2. We can connect our App to this store by importing {connent} from react-redux.
3. We use App as a container component that houses our other components, usually presentational components.
4. In App, we can use mapStateToProps function(the store gives us access to this function) to get state, turn it into prop(s), and send the prop(s) to the components that are inside of our render function. (state to props)
5. Store also gives us access to mapDispatchToProps function that lets us pass an action-creator as a prop to other components. (action to props)
6. Thunk is middleware used for asynchronous calls, like fetch, in Redux. 

I have a lot more reading to do and videos to watch to feel more comfortable before I start my React-Redux final project. If i can stay focused and on task I am sure I will succeed. 

