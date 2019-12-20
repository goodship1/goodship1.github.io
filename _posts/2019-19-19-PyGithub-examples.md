---
layout: post
---

An collection of PyGithub examples.


{%highlight python %}

import pygithub
github =  Pygithub("your access token")

#Get user inforamtion 
user_info = github.get_user()
#get repos of the users
user_info.get_repos()

{% end highlight %}

