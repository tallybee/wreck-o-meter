# Overview

This is a tool to measure how popular on Instagram a capital city is, returning either "HIGH" or "LOW" score. For those with low score but high population density, it gives a warning that it might still be crowded. Have fun! 

### How to run this locally:

* git clone 
* npm install
* npm run start

You'll need an API key to use this, which you can create [here](https://developers.google.com/custom-search/v1/overview)... or email talbondareva@gmail.com (who is currently working on proper authorisation) for one :-)

### The algorithm

This app uses Google Custom Search to gather Instagram hashtag data, getting the number of pure English hashtags (e.g. #berlin rather than #berlingermany or #berlin🇩🇪). It then requests the city area and population. To get the popularity of hashtag, it divides number of times hashtagged by area. A score of over 100 returns HIGH popularity. 
![](./gifs/Berlin.gif)

In addition, it returns population density. In cases of low popularity, but high population density, a note that the city is crowded is displayed. The UN definition of [high population density](http://www.demographia.com/db-worldua.pdf) is used.

![](./gifs/Dhaka.gif)

