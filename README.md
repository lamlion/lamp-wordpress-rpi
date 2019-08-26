# lamp-wordpress-rpi
LAMP Server with Wordpress on Raspberry PI

---
# 1. INSTALL APACHE WEB SERVER

`sudo apt-get install apache2 -y`

`sudo systemctl start apache2`

Check if Apache web server is running
From Raspberry PI desktop in Chromium browser: (http://localhost)
From other location e.g. laptop on the same wifi network: http://<ip-address_of_raspberrypi> (replace <..> 
with ip address found by typing "hostname -I" in terminal on Raspberry PI. E.g. (http://192.168.2.146)

# 2. INSTALL PHP

`sudo apt-get install php -y`

# 3. CREATE PHP TEST SCRIPT

`echo "<?php phpinfo(); ?>" | sudo tee /var/www/html/phpinfo.php`

# 4. TEST PHP SCRIPT FROM A BROWSER

From Raspberry PI desktop in Chromium browser: 

http://localhost/phpinfo.php

From other location e.g. laptop on the same wifi network: http://<ip-address_of_raspberrypi> (replace <..> 
with ip address found by typing "hostname -I" in terminal on Raspberry PI. E.g. (http://192.168.2.146/phpinfo.php)
The result shoud a long web page showing the PHP version along with a lot of configuration details

# 5. INSTALL MARIADB DATABASE (replacement of MySQL Server for smooth installation on Raspbian Buster)
`sudo apt-get install mariadb-server php-mysql -y`

# 6. DOWNLOAD AND UNZIP WORDPRESS (latest version @ (https://wordpress.org/)
`wget https://wordpress.org/latest.tar.gz -O /tmp`
`sudo tar zxvf /tmp/latest.tar.gz /var/www/html/
