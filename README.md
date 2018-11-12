# Awesome python3 webapp to manage personal blogs.
======================


## Some overview screenshots
### The main page
![alt text](https://github.com/Alanlande/Python-web-blog-app/blob/master/pics/Overview_Screen_Shot.png "The main page")



### The blog creation page
![alt text](https://github.com/Alanlande/Python-web-blog-app/blob/master/pics/Blog_Create_Screen_Shot.png "The blog creation page")


## A brief intro:
- Nginx：high performance web server & reverse proxy
- Supervisor：supervise the server process
- MySQL：database
- WatchDog: support automatic fast-launch debugging for development process
- Web framework: I used asychttp, which is the HTTP framework based on asyncio. asyncio can support single-thread high concurrent IO. On the server side: HTTP is IO operation, hence we can utilize single-thread +coroutine to support heavy concurrent requests from multiple users.


## How to deploy:
### Linux server side:
- Install necessary packages:
  ```sh
  $ sudo apt-get install nginx supervisor python3 mysql-server
  $ sudo pip3 install jinja2 aiomysql aiohttp
  ```
- Map the database schema:
  ```sh
  $ mysql -u root -p < schema.sql
  ```
- Configure Supervisor and Nginx on your server: put config/awesome onto /etc/nginx/sites-available/, put config/awesome.conf onto /etc/supervisor/conf.d/


### PC dev side:
- Install fabric to support auto deploy:
  ```sh
  $ pip install 'fabric<2.0'
  ```
- Build and depoly the project onto your server:
  ```sh
  $ fab build
  $ fab deploy
  ```


