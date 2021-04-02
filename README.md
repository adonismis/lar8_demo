git clone https://github.com/adonismis/lar8_demo.git

### 主機元件安裝
```
sudo apt install composer


sudo apt install nodejs
sudo apt install npm
nodejs -v

cd ~
curl -sL https://deb.nodesource.com/setup_12.x -o nodesource_setup.sh
nano nodesource_setup.sh
sudo bash nodesource_setup.sh
sudo apt install nodejs
nodejs -v
```


### 程式安裝
```
sudo composer install

sudo npm install

sudo cp .env.example .env
sudo chmod -R 777 storage 
sudo chgrp -R www-data storage bootstrap/cache
sudo chmod -R ug+rwx storage bootstrap/cache

sudo php artisan key:generate

php artisan migrate

php artisan cache:clear 
composer dump-autoload

a2enmod negotiation
```

### 程式產生器
```
$ php artisan make:scaffold Projects --schema="name:string:index,description:text:nullable,subscriber_count:integer:unsigned:default(0)"
```

### 回復
回復DB-migrate：
```
$ php artisan migrate:rollback
```
還原修改文件到原始狀態：
```
$ git checkout . 
```
可以看的出來剩下是新建的文件，接下來使用下面命令還原：
```
$ git clean -f -d 
```

