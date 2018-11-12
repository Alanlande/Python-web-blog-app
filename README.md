# Awesome python3 webapp to manage personal blogs.
======================


## Some overview screenshots
### The main page
![alt text](https://github.com/Alanlande/Python-web-blog-app/blob/master/pics/Overview_Screen_Shot.png "The main page")



### The blog creation page
![alt text](https://github.com/Alanlande/Python-web-blog-app/blob/master/pics/Blog_Create_Screen_Shot.png "The blog creation page")


## A brief intro:
*Nginx：high performance web server & reverse proxy
*Supervisor：supervise the server process
*MySQL：database
*web framework: I used asychttp, which is the HTTP framework baed on asyncio. asyncio can support single-thread high concurrent IO. On the server side: HTTP is IO operation, hence we can utilize single-thread +coroutine to support heavy concurrent requests from multiple users.
