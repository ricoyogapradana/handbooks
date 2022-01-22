# Handbook's laravel!

**The Laravel Installer**

    composer global require laravel/installer
    laravel new example-apps
    cd example-app
    php artisan serve //to start the server

**Laravel Directory Structure**

Controller Folder Directory

> App\Http\Controller\

Views Folder Directory

> Resources\Views\

Routes File Directory

> App\Routes\Web.php

**Routing**
import the controller file

    use App\Http\Controllers\PostController;

implement route from controller index is function of controller. post is url to process.

    Route::get('/post', [PostController::class, 'index']);

implement route from controller but use all function.

    Route::resource('/post/{id}', PostController::class);

**Controller**

- Create Controller

  create controller name:PostController

  > php artisan make:controller PostController

  create controller with resource from laravel

  > php artisan make:controller --resource PostController

**Laravel Command**
help command by laravel for want you to do

> php artisan

to check the route

> php artisan route:list

create controller name:PostController

> php artisan make:controller PostController

create controller with resource from laravel

> php artisan make:controller --resource PostController
