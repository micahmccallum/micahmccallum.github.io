---
layout: post
title:      "My Experience With The Ruby CLI Gem Project and What I Learned"
date:       2020-05-18 00:31:07 -0400
permalink:  my_experience_with_the_ruby_cli_gem_project_and_what_i_learned
---


To start, just let me say that this project was a lot of fun; no joke!  I can't say that at any time I felt overwhelmed, especially since I was told from the beginning that "it takes most full time (40+ hrs/week) students between 3-7 days to complete" (according to the instructions for the project at learn.co). This project was really a way to bring together all that I had been taught in the previous weeks about Object Oriented Ruby.   Since I only study part time I figured that I was doing pretty well when, after less than a week, I had finished, or that's what I thought.  Let me explain.

It is true that after a week I had a fully functional Ruby CLI Gem that did exactly what it was designed to do.  I chose to use the United States Weather.gov to scrape for weather data.  Weather.gov has an API that does not handle [geocoding](https://en.wikipedia.org/wiki/Geocoding), therefore I needed to use a geocoding service.  I ended up using a gem called [geocoder](http://www.rubygeocoder.com/) which works very well, however, it involves scraping the document that is returned after the geocoder is called.  After getting latitude and longitude for a certain location, these can be used to get a forecast.  The document that is returned is easy enough to scrape but I started to notice a few problems. (Because nothing is that easy!)

Foremost was the issue with the missing screencast.  I got so involved in researching the project that when I made my initial gem I found myself coding along happily. Before I knew it, I was finished with "version 0.1.0" and had no screencast to show. (A requirement for the project is a half-hour screencast.)  What could I do?  Start from scratch? No.  I decided to add another feature:  weather alerts, which makes a lot of sense.  What weather app is any good if it tells you tomorrow's high temperature but does not say anything about a tornado watch today?

>  I always need to have a plan which includes all requirements for a given project.  This includes *good communication*.

Unfortunately, to add alerts to the gem I need to scrape a separate document; and in order to get that document I need to access yet another document.  I also noticed that what I thought were current observations were just a forecast for the current period.  For example, the temperature shown for the evening was the forecast low temperature instead of the actual observation.  Now I have to scrape some more, and the units of measure for the scraped data  needs conversion (meters/second to mph for wind speed, centigrade to Fahrenheit for temperature).  

In all it took almost another part-time week to complete all of this and iron out all of the wrinkles. I have my screencast.  But I don't regret the road I took since I learned something very important:  I always need to have a plan which includes all requirements for a given project.  This includes *good communication*.  Today that means a screencast and a blog.  Tomorrow that may mean reporting to a team or perhaps consultation with responsible parties like management or clients.  A project is essentially worthless without good communication.

I will always fondly remember this project; a turning point in my coding life.  I am left with a genuine feeling of accomplishment.  I know that, in comparison to what my future self will be capable of, this is a small and simple app, but I've been told "you never forget your first time".

Feel free to look at the code : [weather_usa](https://github.com/micahmccallum/weather_usa)

