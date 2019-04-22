# Development Image

#### What's included: 
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
* Will be executed command `php composer.phar install`

#### How to run:
* Install docker & docker-compose
* docker-compose up --build -d
* project should be available at [http://localhost](http://localhost)
