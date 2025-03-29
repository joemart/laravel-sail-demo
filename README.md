This is a quick guide on how to install and use Laravel Sail within your Docker container.


<p align="center">
<a href="https://www.docker.com/"><img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Icon"></a>
<a href="https://laravel.com/"><img src="https://img.shields.io/badge/laravel-%23FF2D20.svg?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel Icon"></a>

</p>

## Technologies you'll need installed

1) <a href="https://getcomposer.org/">Composer</a>
2) <a href="https://www.docker.com/">Docker</a>

## Laravel Sail

To execute Laravel Sail in your docker container follow the commands below:
 > (skip this first step if you already have a project in docker with laravel sail)
* `compose create-project laravel/laravel *name-of-your-project*` 

* Within the *composer.json* file directory, execute `composer require laravel/sail --dev`

* `php artisan sail:install`

* `./vendor/bin/sail up -d` (RUN THIS COMMAND FROM <a href="https://ubuntu.com/desktop/wsl">WSL</a>)


## Vite

To run Vite in your Laravel Sail docker container follow the steps below:

* `./vendor/bin/sail npm install`

* Add this `Vite` line to your *resources/views/welcome.blade.php* file

```php
@vite(['resources/css/app.css', 'resources/js/app.js'])
```
* `./vendor/bin/sail npm run dev`