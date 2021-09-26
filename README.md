# flask_webapp
basic_notes_app

## Install Lamp (linux mint)

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
sudo reboot

sudo apt-get install lamp-server^
```

## Setup Mysql

Change mysql root password

```
sudo mysql -u root

ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'mYSuP3rP8$$';
exit

sudo mysql -u root -p
mYSuP3rP8$$
```


## Check PHP install

make a file in /var/www/html/index.php

```
<? php phpinfo(); ?>
```

## Install phpmyadmin

```
sudo apt-get install phpmyadmin

# Fix instlal
sudo nano /etc/apache2/apache2.conf
# Add the line to the end of the file
include /etc/phpmyadmin/apache.conf
# Restart apache and test http://localhost/phpmyadmin


```
