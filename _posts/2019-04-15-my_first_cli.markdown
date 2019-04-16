---
layout: post
title:      "My First CLI"
date:       2019-04-15 22:19:06 -0400
permalink:  my_first_cli
---


> Here I am! Being put to my first test! My first assessment. Where do I start? I'm super excited but I'm super nervous. I actually do not know where to start. So I read the instructions and started to watch sample walkthrough videos. I thought, hey this isn't so bad. I can do that too! So all the while, I'm brainstorming topics that I want to build my cli on. Ahhh hah moment revealed ----> "WEATHER"! Everyone wants to know the weather outside, let's do that. But then I thought some more and said hey, how about I choose another topic where I can get all sorts of neat facts that will be useful to the public. And there I came up with "United States Facts". I had it all in my head. I want to build a command line inferface that accomplishes the following:

* Design a unique portal that reveals a list of the 50 United States
* Greets the User
* Lets the user choose a state that they would like to get more information about
* Based on their input, the CLI will run capturing the input of the user with the corresponding details of that input
* Gives the user all the facts about the United States -> Hey I can make these attributes (thinking out loud!)
* Gives the user the option to choose another state as many times as they'd like
* Captures the wrong input and says "Hey, Invalid input, please try again!"
* Gives the user the option to exit the CLI following command prompts


*So I had my structure. Now I'm excited to build. *

Helpful **Videos** I replayed over and over: (Just a few favorites)


   * [How to build your gem using bundler](https://www.youtube.com/watch?time_continue=317&v=YZNXWWHUO-E)
   
   * [Sample CLI walkthrough](https://www.youtube.com/watch?v=_lDExWIhYKI)

   * [Building a Ruby Gem from scratch](https://www.youtube.com/watch?v=j0wKePpNlZc&t=20s)

   * [Web Scrapping in Ruby](https://www.youtube.com/watch?v=HacxIKI7yh8)


**Cool Repl.it - CLI**

Here's a Repl.it that I used hand and hand with my project. It helped me with case input commands:

   [Jukebox_CLI](https://repl.it/@natgit/JUKEBOX-CLI)

Now I can really begin. So now I have to scrape! Boy was that fun! --> NOT!! But it was really cool to explore and learn. Once you're able to hit that binding.pry and capture all of that 'behind the scenes' work, it becomes less daunting!
But trust me, I still got some assistance with this part. Several videos and a few zoom sessions with a colleague worked wonders.

**Building the CLI**

Super Fun! I loved playing around with my methods, researching new and cook tricks, and utilizing several techniques I learned e.g: arrays, attr_accessors, .upcase, .downcase, to_i, include?, "\n ", .gsub, <<,  !,  | | , input = gets.chomp 

**Tough Part** 

Incorporating my webscrapping with my CLI. It was tough at first but with some tremendous tips from a colleague, it made it that much easier to understand. Here's how I felt when debugging! 

![](https://cdn-images-1.medium.com/max/1600/1*_XUhAqj85kVNgy9JLlH9Iw.gif)


**GOAL**

I'm going to attempt building another CLI for fun! This time I can utilize what I learned from this project

**End Result**

Hey check out my repo: [US_CLI](https://github.com/mtruman92/us_cli.git)

#####                                                                                             ~Enjoy getting facts about the United States!~

