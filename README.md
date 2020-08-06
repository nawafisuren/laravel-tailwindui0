## Project Description

https://medium.com/teknomuslim/getting-started-tailwind-ui-with-laravel-482f65fd6ef0
http://fathomless-caverns-92546.herokuapp.com/
http://fathomless-caverns-92546.herokuapp.com/teams
http://fathomless-caverns-92546.herokuapp.com/login


Just wondering how amazing Tailwindui is able to create such many beautiful ui component. As a former backend engineer who familiar with Laravel, I want to play around with Tailwindcss and Tailwindui (only free / open component) in this project.

Visit [Demo App](http://fathomless-caverns-92546.herokuapp.com/login) to view the result.

## Stacks

- [Laravel 7](https://laravel.com/)
- [Tailwindcss](https://tailwindcss.com/)
- [Tailwind CSS Frontend Preset for Laravel](https://github.com/laravel-frontend-presets/tailwindcss)
- [Tailwindui](https://tailwindui.com/)
- [Alpinejs](https://github.com/alpinejs/alpine)

## Installation

1. Clone this repository
2. run `composer install`
3. run `npm install`
4. run `php artisan serve` to start your web app
5. Just fill random email and password to login


========================
autoidle/laravel5-heroku 
https://github.com/autoidle/laravel5-heroku


# Laravel on Heroku

Laravel with best practices for deployment on Heroku. [Our articles on Medium](https://medium.com/@AutoIdle)

# Works out of the box

## Features

* `Heroku Postgres` (for Database)
* `Heroku Redis` (for Cache, Queue and Session) 
* Migrate Database automatically on deploy
* Logging
* With Scheduler

## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/autoidle/laravel5-heroku)

![Create New App - Heroku](https://raw.githubusercontent.com/autoidle/laravel5-heroku/master/doc/heroku.png)


## Setup locally and deploy to Heroku

### 1. Install Heroku CLI

https://devcenter.heroku.com/articles/heroku-cli

### 2. Create a new project 

```
composer create-project autoidle/laravel5-heroku my-laravel-heroku
```

### 3. Tracking your app in Git

```
cd my-laravel-heroku
git init
git add .
git commit -m 'Fresh Laravel installation'
```

### 4. Add Heroku app

```
heroku create my-laravel-heroku --region eu --addons=heroku-postgresql:hobby-dev,heroku-redis:hobby-dev
```

### 5. Set ENV variables

```
heroku config:set APP_DEBUG=true
heroku config:set APP_KEY=$(php artisan --no-ansi key:generate --show)
```

### 6. Push your code to laravel

```
git push heroku master
```

### 7. Checkout your Laravel installation on Heroku

```
heroku open
```

### 8. Checkout the log (Optional)

```
heroku logs -t
```

## Extend with Laravel Auth (Optional)

### 1. Laravel provides a quick way to scaffold all of the routes and views you need for authentication using one simple command:

```
php artisan make:auth
```

### 2. Add changes to Git

```
git add .
git commit -m 'Add Laravel Auth'
```

### 3. Deploy to Heroku

```
git push heroku master
```

### 4. Checkout your Laravel installation on Heroku with Auth

```
heroku open
```


![Laravel with Auth on Heroku (Registration)](https://raw.githubusercontent.com/autoidle/laravel5-heroku/master/doc/register.png)

![Laravel with Auth on Heroku (Logged in)](https://raw.githubusercontent.com/autoidle/laravel5-heroku/master/doc/home.png)

---

[Code difference between Laravel and Laravel on Heroku](https://github.com/autoidle/laravel5-heroku/compare/84ce504...master)

---

We are building a Heroku Add-on that helps you save money by automatically putting your non-critical apps to sleep after a period of inactivity.

[AutoIdle on the Heroku Marketplace](https://elements.heroku.com/addons/autoidle)


https://github.com/autoidle/laravel5-heroku

autoidle/laravel5-heroku 

========================




===============================
 jessedc laravel-heroku-example 
 https://github.com/jessedc/laravel-heroku-example/blob/master/readme.md
  
 
## Heroku Laravel Example

This is boilerplate Laravel 5.7 project similar to what the `laravel new` or `composer create-project` commands create.

This project can be used as is as a shortcut to deploying a Laravel 5.6 app on heroku, or used as a guide.

## Heroku Specific Configuration

- [Procfile](https://devcenter.heroku.com/articles/procfile) defining a web process using nginx and a worker process for running queues
- Database configuration defaults set to use Postgres and to parse heroku-postgres `DATABASE_URL` environment variable
- Redis configuration setup to use heroku-redis `REDIS_URL` environment variable
- Failed job database configuration defaulting to postgres
- A heroku app.json and post-deployment script (`php artisan postdeploy:heroku`)for use with Heroku Review Apps
- TrustedProxies middleware configured to trust Heroku load balancers correctly
- npm task named "postinstall" that is run during heroku deployments
- Heroku specific logging configuration set as the default.  

## Additional Configuration

- Pinned to PHP 7.2 (`~7.2.0`)
- Setup with bootstrap scaffolding (`php artisan preset bootstrap`)

## Local Development

**1. Database, app key, .env**

Clone this repository and run the following commands:

```bash
composer install
cp .env.example .env
touch database/database.sqlite
php artisan key:generate
php artisan migrate
npm install 
npm run dev
```

**2. Run**

```bash
php artisan serve
```

## Deploying to Heroku

**1. Create a Heroku app**

Create an app name

```bash
app_name=heroku-laravel57-test-app
```

Create Heroku app

```bash
heroku apps:create $app_name
heroku addons:create heroku-postgresql:hobby-dev --app $app_name
heroku addons:create heroku-redis:hobby-dev --app $app_name
heroku buildpacks:add heroku/php --app $app_name
heroku buildpacks:add heroku/nodejs --app $app_name
```

**2. Add Heroku git remote**

```bash
heroku git:remote --app $app_name
```

**3. Set config parameters**

For Laravel to operate correctly you need to set `APP_KEY`:

```bash
heroku config:set --app $app_name APP_KEY=$(php artisan --no-ansi key:generate --show)
```

Set Queues, sessions and cache to use redis

```bash
heroku config:set --app $app_name QUEUE_CONNECTION=redis SESSION_DRIVER=redis CACHE_DRIVER=redis
```

Optionally set your app's environment to development

```bash
heroku config:set --app $app_name APP_ENV=development APP_DEBUG=true APP_LOG_LEVEL=debug
```

**4. Deploy to Heroku**

```bash
 git push heroku master
```

**5. Run migrations**

```bash
heroku run -a $app_name php artisan postdeploy:heroku
```

---

## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

 
 jessedc laravel-heroku-example 
 https://github.com/jessedc/laravel-heroku-example/blob/master/readme.md
 
 ===============================
 
 
 //////////////////////////////////
  MikeRogers0/Heroku-Laravel-CRUD-demo
https://github.com/MikeRogers0/Heroku-Laravel-CRUD-demo/edit/master/readme.md
 # Heroku CRUD Demo

## How I got to here

I followed the tutorials [Deploying a Laravel Application to Heroku](http://www.easylaravelbook.com/blog/2015/01/31/deploying-a-laravel-application-to-heroku/) & [Installing a Laravel app on Heroku](https://mattstauffer.co/blog/installing-a-laravel-app-on-heroku).

I then installed a [crud-generator](https://packagist.org/packages/appzcoder/crud-generator) to make generating scaffolding easy.

## Things to run before we start

Add the buildpack to tell Heroku we are PHP app and not a node app

    heroku config:add BUILDPACK_URL=https://github.com/heroku/heroku-buildpack-php

Then add the laravel config keys

    heroku config:add APP_KEY=f9F8w6B0sQnXK94vCgM2fh76ewMKE7Hp &&
    heroku config:add APP_DEBUG=true

Then lets make a database!

    heroku addons:create heroku-postgresql:hobby-dev

## Making our CRUD

    php artisan crud:generate Person --fields="name:string, email:string, phone:integer, message:text"

Add the route

    Route::resource('person', 'PersonController');

Deploy up to heroku, then run

    php artisan migrate


 MikeRogers0/Heroku-Laravel-CRUD-demo
https://github.com/MikeRogers0/Heroku-Laravel-CRUD-demo/edit/master/readme.md
 \\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\

