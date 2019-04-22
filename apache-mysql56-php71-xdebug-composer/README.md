# Development Image

#### What is included: 
* Apache
* MySQL 5.6
* PHP 7.1
  * mysqli
  * mbstring
  * pdo_mysql
  * xdebug 2.6
  * zip
  * mod_rewrite enabled
* composer

#### Auto initializing when container is started:
* MySQL
    * To be created on image startup
        * new database `someDB`
        * new user `testuser` with password `testpassword` and full access to `someDB`  [Read more...](https://docs.docker.com/samples/library/mysql/#environment-variables)
    * Will be executed all SQL files in folder resources. [Read more...](https://docs.docker.com/samples/library/mysql/#initializing-a-fresh-instance)
* Will be executed executed command `php composer.phar install`

#### How to run:
* Install docker & docker-compose
* docker-compose up --build -d
* project homePage should be available at [http://localhost](http://localhost)


#### Additional Information
* [Quickstart with Docker + xdebug (PhpStorm)](https://blog.jetbrains.com/phpstorm/2018/08/quickstart-with-docker-in-phpstorm/)
* [Full Docker Help (PhpStorm)](https://www.jetbrains.com/help/phpstorm/docker.html)
