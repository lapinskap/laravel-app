<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

# laravel-app
> Here goes your awesome project description!

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshots)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Inspiration](#inspiration)
* [Contact](#contact)

## General info
Add more general information about project. What the purpose of the project is? Motivation?

## Screenshots
![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen1.jpg)

![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen2.jpg)

![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen3.jpg)

![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen4.jpg)

## Technologies
* Laravel 5.5 - PHP framework
* Some Bootstrap

## Setup
Type in your terminal: 
```
$ git clone https://github.com/lapinskap/laravel-app.git
$ cd laravel-app
$ composer update
```
> "$" is not part of a command, just bash symbol

Next: Configure the database in the .env file - mine is `pgsql`
```
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=laravel55
DB_USERNAME=postgres
DB_PASSWORD=postgres
```
> Probably you'll need to create your own (blank) database, then type it's name in `.env` file. Php will create tables inside. 

Start the Laravel development server:
```
$ php artisan serve
```
Finally: Switch to the URL: http://localhost:8000/products/create

## Code Examples
Show examples of usage:
`put-your-code-here`

## Features
List of features ready and TODOs for future development
* Awesome feature 1
* Awesome feature 2
* Awesome feature 3

To-do list:
* Wow improvement to be done 1
* Wow improvement to be done 2

## Status
Project is: _in progress_, _finished_, _no longer continue_ and why?

## Inspiration
Add here credits. Project inspired by..., based on...

## Contact
Created by [@lapinskap](https://www.facebook.com/paulina.lapinska99) - feel free to contact me!

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
