---
layout: post
title:      "My Experience With The Ruby CLI Gem Project and What I Learned"
date:       2020-05-18 04:31:07 +0000
permalink:  my_experience_with_the_ruby_cli_gem_project_and_what_i_learned
---


To start, just let me say that this project was a lot of fun; no joke!  I can't say that at any time I felt overwhelmed, especially since I was told from the beginning that "it takes most full time (40+ hrs/week) students between 3-7 days to complete" (according to the instructions for the project at learn.co).  Since I only study part time I figured that I was doing pretty well when after less than a week I had finished, or that's what I thought.  Let me explain.

It is true that I had a fully functional Ruby CLI Gem that did exactly what it was designed to do.  I chose to use the United States Weather.gov to scrape for weather data.  Weather.gov has an API that does not handle [geocoding]https://en.wikipedia.org/wiki/Geocoding) thus I needed to use a geocoding service.  I ended up using a gem called [geocoder](http://www.rubygeocoder.com/) which works very well, however it involves scraping the document that is returned after the geocoder is called.  After getting latitude and longitude for a certain loctation these can be used to get a forecast.  The document that is returned is also easy enough to scrape but I started to notice a few problems. (Because nothing is that easy!)

Foremost was the issue with the missing screencast.  I got so involved in researching the project and when I made my initial gem I found myself coding along happily. Before I knew it, I was finished with version 0.1.0 and had no screencast to show. (A requirement for the project is a half-hour screencast.)  What could I do?  Start from scratch? No.  I decided to add another feature:  weather alerts, which makes a lot of sense.  What weather app is any good if it tells you tomorrow's high temperature but does not say anything about a tornado watch?


