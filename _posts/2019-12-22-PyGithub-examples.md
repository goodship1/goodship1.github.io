
---
layout: post
---



Pygithub examples while developing an issue tracker using pygithub ive seen alot people are seeking on how to use the api.So over the holiday peroid i will be writing a short guide on some of useful features of the api.




{% highlight python %}


import pygithub
my_github = pygithub("your token")


#get user information from github api

users = my_github.get_user() #get user information
print(user.name)#prints the name of the github account 
print(user.email)#prints the users email address

#getting repo and commit  information
 repo = user.get_repos()
 commits = repo.get_commits()
 
  
{% endhighlight %}
