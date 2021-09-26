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

# Fix install
sudo nano /etc/apache2/apache2.conf
# Add the line to the end of the file
include /etc/phpmyadmin/apache.conf
# Restart apache and test http://localhost/phpmyadmin
```

Add missing packages for php8.0

```
apt-get -y install \
    libapache2-mod-php8.0 \
    libphp8.0-embed \
    php8.0 \
    php8.0-apcu \
    php8.0-bcmath \
    php8.0-bz2 \
    php8.0-cgi \
    php8.0-cli \
    php8.0-common \
    php8.0-curl \
    php8.0-fpm \
    php8.0-gd \
    php8.0-imagick \
    php8.0-imap \
    php8.0-intl \
    php8.0-mbstring \
    php8.0-memcache \
    php8.0-mysql \
    php8.0-opcache \
    php8.0-pspell \
    php8.0-raphf \
    php8.0-soap \
    php8.0-tidy \
    php8.0-uuid \
    php8.0-xml \
    php8.0-xsl \
    php8.0-yaml \
    php8.0-zip
```

---

# Flask install

## Setup virtual env

```
# Using python3
sudo apt install -y python3-pip
sudo apt install build-essential libssl-dev libffi-dev python-dev
sudo apt install -y python3-venv

python3 -m venv flask_blog/

source flask_blog/bin/activate

# Now in virtual Env (env)
(env)pip install flask

# Check flask version 
python -c "import flask; print(flask.__version__)"
```


Original Guide:   
https://www.digitalocean.com/community/tutorials/how-to-make-a-web-application-using-flask-in-python-3  
https://www.geeksforgeeks.org/connect-flask-to-a-database-with-flask-sqlalchemy/  
