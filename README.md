first before running the project download laravel save the startup files in the viwes and web.php in routes and auth in controllers 1. Check System Requirements Laravel requires:

PHP ≥ 8.1

Composer (Dependency Manager)

Required PHP Extensions:

OpenSSL, PDO, Mbstring, Tokenizer, XML, Ctype, JSON, BCMath

To check PHP version:

bash Copy Edit php -v 2. Install Composer Laravel uses Composer to manage dependencies.

Windows: Download Composer: getcomposer.org/download

Install and check:

bash Copy Edit composer -V Linux / Mac: bash Copy Edit sudo apt update && sudo apt install php-cli unzip curl curl -sS https://getcomposer.org/installer | php sudo mv composer.phar /usr/local/bin/composer composer -V 3. Install Laravel You have two main ways:

(a) Using Laravel Installer bash Copy Edit composer global require laravel/installer laravel new project_name Make sure Composer’s global bin directory is in your PATH. (On Linux/Mac: add export PATH="$HOME/.composer/vendor/bin:$PATH" in .bashrc)

(b) Using Composer Create-Project bash Copy Edit composer create-project laravel/laravel project_name 4. Set Permissions (Linux/Mac only) Give storage and bootstrap/cache directories write permission:

bash Copy Edit sudo chmod -R 775 storage bootstrap/cache 5. Run Laravel Development Server bash Copy Edit cd project_name php artisan serve Then open: 👉 http://localhost:8000

Configure Environment Copy .env.example to .env:
bash Copy Edit cp .env.example .env Generate an app key:

bash Copy Edit php artisan key:generate
