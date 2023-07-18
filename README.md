<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://github.com/ehsanSepahi/toDo/assets/71543126/fd20f62f-50dc-47aa-9f0a-c55740d5142a" width="150" alt="Laravel Logo"></a></p>

<!-- <p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://github.com/ehsanSepahi/toDo/assets/71543126/cee10d3e-41d0-42fd-ae15-8a0c77d24b54" width="20" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p> -->


# Getting started

## Intro

The Book Management API project is a simple RESTful API application built using Laravel, allowing you to manage books through HTTP requests and responses. This project serves as an illustrative example to demonstrate the capabilities of the Laravel framework in creating a basic RESTful API.

Key features of this project include:

1. Book Model: Creation of a "Book" model with attributes such as title, author, and publication year.

2. BookController: Implementation of CRUD (Create, Read, Update, Delete) methods to manage books.

3. API Routes: Definition of API routes for performing CRUD operations on books, specifically the /api/books endpoint.

4. Migration and Database: Creation of a "books" table to store book information using migrations, along with database connection settings in the .env file.

5. Routes and Requests: Definition of routes related to book management (GET, POST, PUT, DELETE) and the corresponding request handling.

By running this project, you will be able to interact with book data by sending various requests to the API. Features such as creating new books, retrieving lists of books, updating book information, and deleting books will be available. Additionally, this project can be easily extended to add custom features as per your requirements.

## Installation

Please check the official laravel installation guide for server requirements before you start. [Official Documentation](https://laravel.com/docs/5.4/installation#installation)

Alternative installation is possible without local dependencies relying on [Docker](#docker). 

Clone the repository

    git clone git@github.com:ehsanSepahi/RESTFull-API.git

Switch to the repo folder

    cd RESTFull-API

Install all the dependencies using composer

    composer install

Copy the example env file and make the required configuration changes in the .env file

    cp .env.example .env

Generate a new application key

    php artisan key:generate
    
Edit env file

    nano .env

Run the database migrations (**Set the database connection in .env before migrating**)

    php artisan migrate

Start the local development server

    php artisan serve

You can now access the server at http://localhost:8000

in vps make sure you have activated the following item 

    sudo a2enmod rewrite
    systemctl restart apache2

**TL;DR command list**

    git clone git@github.com:ehsanSepahi/RESTFull-API.git
    cd RESTFull-API
    composer install
    cp .env.example .env
    php artisan key:generate
    nano .env
    
**Make sure you set the correct database connection information before running the migrations** [Environment variables](#environment-variables)

    php artisan migrate
    php artisan serve
    
    
## Docker

To install with [Docker](https://www.docker.com), run following commands:

```
git clone git@github.com:ehsanSepahi/RESTFull-API.git
cd RESTFull-API
cp .env.example.docker .env
docker run -v $(pwd):/app composer install
cd ./docker
docker-compose up -d
docker-compose exec php php artisan key:generate
docker-compose exec php php artisan migrate
docker-compose exec php php artisan serve --host=0.0.0.0
```

The RESTFull-API can be accessed at [http://localhost:8000](http://localhost:8000).

## RESTFull-API Specification

In this guide we will walk through building a modern Laravel application from scratch. 
You can login into system and make a chirp

----------

## Folders

- `app` - Contains all the Eloquent models
- `config` - Contains all the application configuration files
- `database/migrations` - Contains all the database migrations
- `routes` - Contains all the api routes defined in api.php file
- `tests` - Contains all the application tests

## Environment variables

- `.env` - Environment variables can be set in this file

***Note*** : You can quickly set the database information and other variables in this file and have the application fully working.

----------

# Testing

Run the laravel development server

    php artisan serve

The api can now be accessed at

    http://localhost:8000
