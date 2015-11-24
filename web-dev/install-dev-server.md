# List of commands for web server setup on Ubuntu

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install vim
```

## Apache

```
sudo apt-get install apache2
```

## NodeJS and NPM

```
sudo apt-get install nodejs
sudo apt-get install npm
```

## PHP
```
sudo apt-get install php5
```

## MongoDB

```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
sudo apt-get update
sudo apt-get install -y mongodb-org
echo "mongodb-org hold" | sudo dpkg --set-selections
echo "mongodb-org-server hold" | sudo dpkg --set-selections
echo "mongodb-org-shell hold" | sudo dpkg --set-selections
echo "mongodb-org-mongos hold" | sudo dpkg --set-selections
echo "mongodb-org-tools hold" | sudo dpkg --set-selections
```

## Fix Rights

```
sudo chmod 777 /var/www/ -R
sudo chown www-data:www-data /var/www/ -R
sudo usermod -a -G www-data nicolas
```

## Symfony

```
cd /var/www
wget http://symfony.com/download?v=Symfony_Standard_Vendors_2.3.3.tgz
tar -zxvf download?v=Symfony_Standard_Vendors_2.3.3.tgz
cd Symfony
sudo chown -R root:www-data app/cache
sudo chown -R root:www-data app/logs
sudo chown -R root:www-data app/config/parameters.yml
sudo chmod -R 775 app/cache
sudo chmod -R 775 app/logs
sudo chmod -R 775 app/config/parameters.yml
```

or

```
sudo curl -LsS http://symfony.com/installer -o /usr/local/bin/symfony
sudo chmod a+x /usr/local/bin/symfony
```

Fix rights

```
HTTPDUSER=`ps axo user,comm | grep -E '[a]pache|[h]ttpd|[_]www|[w]ww-data|[n]ginx' | grep -v root | head -1 | cut -d\  -f1`
sudo setfacl -R -m u:"$HTTPDUSER":rwX -m u:`whoami`:rwX app/cache app/logs
sudo setfacl -dR -m u:"$HTTPDUSER":rwX -m u:`whoami`:rwX app/cache app/logs
```

## Gulp, Bower, ...

```
sudo npm install gulp -g
sudo npm install -g bower 
sudo apt-get install nodejs-legacy
```

## Composer Mongo

```
sudo apt-get install php5 php5-dev libapache2-mod-php5 apache2-threaded-dev php-pear php5-mongo
sudo pecl install mongo
sudo echo "extension=mongo.so" >> /etc/php5/apache2/php.ini
sudo service apache2 restart
```

## Composer Curl

```
sudo apt-get install php5-curl
```

## Module Gulp
```
npm install browser-sync --save-dev
npm install gulp-awspublish --save-dev
npm install --save event-stream
npm install --save mout
npm install --save optimist
npm install --save socket.io
npm install --save di
npm install --save bluebird
npm install --save log4js
npm install --save useragent
npm install --save chokidar
npm install --save expand-braces
npm install --save connect
body-parser
core-js
http-proxy
source-map
estraverse-fb
escope
globals
debug
is-my-json-valid
shelljs


```




