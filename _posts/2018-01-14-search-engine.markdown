---
layout: post
title:  "How to change the search engine dynamically in google chrome?"
date:   2018-01-14 00:08:45
description: How to change the search engine dynamically in google chrome
categories:
- post
tags:
- chrome
- search-engine
---

## Google Chrome
How to quickly search on different search engines?

### Introduction
Sometimes I wonder what will be the search engine result for my query if it is not personalized. As everyone know, google results are personalized based on our pervious searches. So sometimes I use [DuckDuckGo](https://duckduckgo.com).

### About This Post
Say for example, if you want to search `Hello World` in google.com, yahoo.com, bing.com from the chrome search bar without changing the settings then this is correct place you have landed.

I have also added a section if you want to add a new search engine with this dynamically switching feature.

### Modifying The Existing Search Engine
Chrome has few default search engines and you can find them by right clicking the search bar and selecting Edit Search Engines option.

If you want to search on various search engine from the search bar then you can use the keywords mentioned in this settings page. By default it is longer than the actually url. 😀

You can edit the keyword to make it short so typing the couple of character and pressing space bar in the keyboard will change the search engine.

![search-engine-gif](/assets/images/search-engine.gif)

### Adding A New Search Engine
If you want to search in your firm's intranet portal or in github then you can follow the below step to add the search engine. Here I am showing how to add [DuckDuckGo](https://duckduckgo.com)

1. Go to the search engine and search something
2. You will get a URL for the search result
3. Replace the query string with `%s`
2. Right click the Search bar and select Edit Search Engines
2. Click Add button in the Manage Search Engines page
3. Give a name to the Search Engine, in out case `DuckDuckGo`
4. Type a keyword `d!`
5. Paste the modified url in the URL field
6. Test it with your keyword in the search bar

![duckduckgo-gif](/assets/images/duckduckgo.gif)