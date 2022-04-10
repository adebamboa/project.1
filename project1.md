## Awesome Documentation of Project 1

`sudo apt update`

`sudo apt imstall apache2`

`sudo systemctl status apache2`

![Apache-status](./images/Apache-status.PNG)


![ssh-http-inbound settings](./images/ssh-http-%20inbound%20settings.png)


`curl http://localhost:80`


![curl-http.png](./images/curl-http.png)


`http://<Public-IP-Address>:80`


![Apache-defaultpage](./images/Apache-defaultpage.png)


`sudo apt install mysql-server`

`sudo mysql`

![sudo-mysql](./images/sudo_mysql.png)


`mysql> exit` 

`sudo apt install php libapache2-mod-php php-mysql` 

![php_v](./images/php_v.png)

`sudo mkdir /var/www/projectlamp`


` sudo chown -R $USER:$USER /var/www/projectlamp`


`sudo vi /etc/apache2/sites-available/projectlamp.conf`


`<VirtualHost *:80>
    ServerName projectlamp
    ServerAlias www.projectlamp 
    ServerAdmin webmaster@localhost
    DocumentRoot /var/www/projectlamp
    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>`




`sudo ls /etc/apache2/sites-available`


![The San Juan Mountains are beautiful!](./images/ls-command.png)


`sudo a2ensite projectlamp`


`sudo a2dissite 000-default`


`sudo apache2ctl configtest`


`sudo systemctl reload apache2`

`sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html`


`http://<Public-IP-Address>:80`

![Echo-message](./images/echo-message.png)


`http://<Public-DNS-Name>:80`

![Dns-hostname](./images/DNS-hostname.png)


`sudo vim /etc/apache2/mods-enabled/dir.conf`


`<IfModule mod_dir.c>
        #Change this:
        #DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
        #To this:
        DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm
</IfModule>`


`sudo systemctl reload apache2`



`vim /var/www/projectlamp/index.php`


`<?php
phpinfo();`



![Php](./images/php.png)


`sudo rm /var/www/projectlamp/index.php`






