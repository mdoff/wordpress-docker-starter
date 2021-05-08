# Wordpress docker starter
It's just a simple `docker-compose.yml` file that sets up wordpress image with database and phpmyadmin.
It requires folder named `wordpress` in this path (this will be a root directory).

After command
```
docker-compose up
```
on `http://localhost` will be available root directory and phpmyadmin can be accessed on `http://localhost:8181`.

To download wordpress you can use this snippet:
```
wget https://wordpress.org/latest.zip && unzip latest.zip && rm latest.zip
```

After staring docker compose run:
```
sudo chown -R $USER wordpress
```
and then add:
```
define('FS_METHOD', 'direct');
```
to a wp-config.php
