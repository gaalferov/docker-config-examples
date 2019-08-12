# Development image for [Yii2 Framework](https://www.yiiframework.com/

#### What's included: 
* Apache
* MySQL 5.7
* PHP 7.3 with all necessary libraries
* Xdebug
* Composer

#### How to run:
* Install [docker & docker-compose](https://www.docker.com/)
* Copy and customize your docker arguments with command: `cp .env-dist .env`
* Copy your Yii2 project on `app` folder
* Create and set your own [GitHub API Token](https://github.com/settings/tokens) to the field `GITHUB_API_TOKEN` for fixing problem with rate limits
* Run docker build command: `docker-compose up --build -d`
* Run Yii2 migrate command: `docker exec yii2-minify-url_app_1 php yii migrate --interactive=0`
* Url Shortener will be available at [http://localhost](http://localhost)
* PHPMyAdmin available at [http://localhost:8080](http://localhost:8080)
