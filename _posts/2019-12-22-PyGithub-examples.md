
---
layout: post
---



Pygithub examples while developing an issue tracker using pygithub ive seen alot people are seeking on how to use the api.So over the holiday peroid i will be writing a short guide on some of useful features of the api.




{% highlight python %}


import pygithub
my_github = pygithub("your token")


#get user information from github api

my_github.get_user() #get user information
print(my_github.name)#prints the name of the github account 
print(my_github.email)#prints the users email address

#getting repo information
 
  
{% endhighlight %}
