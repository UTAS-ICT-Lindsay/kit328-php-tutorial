FROM php:8.2-apache

# Install standard PHP extensions commonly required for database connections (PDO MySQL)
RUN docker-php-ext-install pdo pdo_mysql

# Enable Apache's mod_rewrite engine (crucial for clean routing and Single Page Apps)
RUN a2enmod rewrite

# Set the working directory to Apache's public document root
WORKDIR /var/www/html

# Copy your frontend PHP/HTML files into the container webroot
COPY . /var/www/html/

# Expose standard web traffic port internally
EXPOSE 80