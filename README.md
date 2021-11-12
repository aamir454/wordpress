# wordpress
WordPress with logs and db on Nginx


We will deploy the 'Wordpress' PHP application with Nginx as the web server, and MariaDB for the MySQL database as docker containers managed by docker-compose. Each application (Wordpress, Nginx, and MySQL) will run in its own container, you can see the list below:

- Nginx: We use the official docker image, latest version 'nginx: latest'.

- Wordpress: Wordpress provides some docker images on docker-hub, and we will use WordPress 4.7 with PHP-FPM 7.0 on it.

- MySQL: We will use MariaDB official container, latest version.

So we need 3 docker images from the docker hub registry.

We will not run docker as root, we will use normal Linux user. So just create a new user with command below (feel free to use a different username here, just ensure the user does not exist yet. If you choose a different name, ensure to change it in all commands that follow in this tutorial):

Make directoris

touch docker-compose.yml

mkdir -p nginx/

mkdir -p db-data/

mkdir -p logs/nginx/

mkdir -p wordpress/
