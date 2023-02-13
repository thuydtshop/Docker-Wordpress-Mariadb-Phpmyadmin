# Docker-Wordpress-Mariadb-Phpmyadmin
Docker with wordpress configuration

### How to use

1. Clone this repository
2. Run `docker compose build && docker compose up -d`
3. Download wordpress and extract it to `./src` folder
4. Run `docker compose exec wordpress bash` and run `chown -R www-data:www-data /var/www/html` if you are using linux
5. Run in your browser `localhost:8080` and follow the installation steps