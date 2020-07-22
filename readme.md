<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="public/images/logo.png" alt="Project logo"></a>
</p>

<h3 align="center">VueBnb</h3>

<div align="center">

  [![Status](https://img.shields.io/badge/status-active-success.svg)]() 
  ![GitHub issues](https://img.shields.io/github/issues/vcjpierre/fullstack-laravel-vuejs)
  [![GitHub Pull Requests](https://img.shields.io/github/issues-pr/vcjpierre/fullstack-laravel-vuejs.svg)](https://github.com/kylelobo/The-Documentation-Compendium/pulls)

</div>

---

<p align="center"> Vuebnb: Full-Stack Vue.js and Laravel App.
    <br> 
</p>

## 📝 Table of Contents
- [About](#about)
- [Getting Started](#getting_started)
- [Built Using](#built_using)
- [Credits](#credits)

## 🧐 About <a name = "about"></a>
Vuebnb, a simple clone of Airbnb.

## 🏁 Getting Started <a name = "getting_started"></a>
These instructions will get you a copy of the project up and running on your local machine for development.

### Prerequisites
Clone the repository

```
git clone https://github.com/gabipetrovay/fullstack-laravel-vuejs.git
```

```
cd fullstack-laravel-vuejs
```

### Create and run the MySQL database

You need to install [Docker](https://hub.docker.com/editions/community/docker-ce-desktop-mac/).

Create a Docker network for the MySQL server:

```shell
docker network create mysql-network
```

Run a MySQL v5 container:

```shell
docker run -p 3306:3306 --rm --network mysql-network --name mysql5 -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:5
```

Create the database (you will be prompted for the `MYSQL_ROOT_PASSWORD` provided above):

```shell
docker run --rm -it --network mysql-network mysql:5 /bin/bash -c "echo 'CREATE DATABASE IF NOT EXISTS vuebnb' | mysql -h mysql5 -u root -p"
```

### Application configuration

You need to create the `.env` file (using inspiration from `.env.example`). The minimum configuration you need is:

```
APP_NAME=Vuebnb
APP_ENV=local
APP_KEY=kkkkkkkkkkkkkkkkkkkkkkkkkkkkkkkk
APP_DEBUG=true
APP_LOG_LEVEL=debug
APP_URL=http://vuebnb.test

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=vuebnb
DB_USERNAME=root
DB_PASSWORD=my-secret-pw
```

### Installation
Install all dependencies

```
composer install
npm install
```

Create your DB and put your environments variables in the file `.env`

Then run migrations and seeders

```
php artisan migrate
php artisan db:seed
```

## ⛏️ Built Using <a name = "built_using"></a>
- [Laravel](https://laravel.com//) - PHP Framework
- [VueJs](https://vuejs.org/) - Web Framework


## 🎉 Credits <a name = "credits"></a>
- https://vuejsdevelopers.com/2017/11/20/vuebnb-full-stack-laravel/
