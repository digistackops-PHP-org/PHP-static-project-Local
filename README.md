## Launch "t2.micro" Ec2 Instance and Open port "8000" in security Group 

# Install PHP
```
sudo yum install -y php php-cli php-common php-mbstring php-xml php-curl php-json php-zip php-devel php-opcache php-pdo php-mysqlnd

php -v
```

# Install Dependencies
```
cd ~
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php composer-setup.php
sudo mv composer.phar /usr/local/bin/composer
php -r "unlink('composer-setup.php');"

composer -V
```
# Get the Code 
```
sudo yum install git -y
sudo git clone https://github.com/digistackops-PHP-org/PHP-static-project-Local.git
cd PHP-static-project-Local/
git checkout 01-Local-setup 
```
# Start your Project
```
composer install
php -S 0.0.0.0:8000 -t public
```
open Browser and Check App is working or Not
```
http://<Your-Public-IP>:8000
```
<img width="686" height="622" alt="image" src="https://github.com/user-attachments/assets/ec61e379-417c-4eae-9014-9d54f7b084e2" />

