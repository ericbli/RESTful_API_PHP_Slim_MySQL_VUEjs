Back End:

1. WAMP installation
2. create directory slim in WWW
3. create database with MySQL
4. enter slim adn use composer    
5. composer require slim/slim
6.
https://www.slimframework.com/


in C:\wamp64\bin\apache\apache2.4.23\conf\extra

edit file: httpd-vhosts.conf to add:

####################################

<VirtualHost *:80>
	ServerName slim
	DocumentRoot c:/wamp64/www/slim/public
	<Directory  "c:/wamp64/www/">
		Options +Indexes +Includes +FollowSymLinks +MultiViews
		AllowOverride All
		Require local
	</Directory>
</VirtualHost>

##########################################

in C:\Windows\System32\drivers\etc
edit file host to add:

##########################

127.0.0.1 slim

##########################
Get:
http://slim/api/customers
http://slim/api/customer/3
Post:
http://slim/api/customer/add
{"first_name":"AAA","last_name":"BBBBBB","phone":"07634433434","email":"mike.svensson@gmail.com","address":"Ljusgatan 34","city":"stockholm","state":"sweden"}

delete:
http://slim/api/customer/delete/10


Front End 


cd frontend
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```
