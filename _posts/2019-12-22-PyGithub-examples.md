---
layout: post
---

An collection of PyGithub examples. Ive currently working on building an issue tracker using pygithub online i have seen alot of people asking for example's on how to use the pygithub api. So over the comming weeks i will adding a comprehensive list of some or the core functionalities of the api.  


{%highlight python %}

import pygithub
github =  Pygithub("your access token")

#Get user inforamtion 
user_info = github.get_user()
#get repos of the users
user_info.get_repos()

{% end highlight %}

