<p align="center"><img src="https://laravel.com/assets/img/components/logo-laravel.svg"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

# laravel-app
> Simple Laravel 5.5 application with CRUD - stores products and its price 

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

By creating this application I wanted to learn some CRUD. This is an interesting comparison to the applications that I created in rails.
These frameworks have many similarities.

It's my first experience with laravel.


## Screenshots

URL: http://localhost:8000/products/create


![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen1.jpg)


If you submit the form without any value then, you can see the errors like below image.


![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen2.jpg)

If you fill all the values then, you will redirect to this page with the success message. 


![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen4.jpg)

URL: http://localhost:8000/products


![Example screenshot](https://raw.githubusercontent.com/lapinskap/laravel-app/master/img/screen3.jpg)

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

Next: Configure the database in the `.env` file - mine is `pgsql`
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

#### Additional setup you may don't know but you already need it
Few things to install:

PHP 7 and Composer:

[Windows 10](http://kizu514.com/blog/install-php7-and-composer-on-windows-10/)

[PostgreSQL](https://www.postgresql.org/) (or another database)

[pgAdmin III](https://www.pgadmin.org/download/)

## Code Examples

app/Http/Controllers/ProductController.php

```php
public function store(Request $request)
    {
          $product = $this->validate(request(), [
            'name' => 'required',
            'price' => 'required|numeric'
          ]);
          Product::create($product);
          return back()->with('success', 'Product has been added');
    }
```


CRUD - update function looks as follows:
```php
public function update(Request $request, $id)
    {
        $product = Product::find($id);
        $this->validate(request(), [
          'name' => 'required',
          'price' => 'required|numeric'
        ]);
        $product->name = $request->get('name');
        $product->price = $request->get('price');
        $product->save();
        return redirect('products')->with('success','Product has been updated');
    }
```
## Features
* PostgreSQL database
* Laravel, yay
* Awesome feature 3?


## Status
Project is: _finished_

## Inspiration
Project based on [Laravel tutorial](https://appdividend.com/2017/08/20/laravel-5-5-tutorial-example/)



## Contact
Created by [@lapinskap](https://www.facebook.com/paulina.lapinska99) - feel free to contact me!

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
