# Handbook's laravel!

**The Laravel Installer**

    composer global require laravel/installer

    laravel new example-apps

    cd example-app

    php artisan serve

---

**Laravel Directory Structure**

Controller Folder Directory

> App\Http\Controller\

Views Folder Directory

> Resources\Views\

Migrations Folder Directory

> Database\Migrations\

Routes File Directory

> App\Routes\Web.php

Database File Directory

> App\Config\Database.php

---

**Routing**

import the controller file

    use App\Http\Controllers\PostController;

implement route from controller index is function of controller. post is url to process.

    Route::get('/post', [PostController::class, 'index']);

implement route from controller but use all function.

    Route::resource('/post/{id}', PostController::class);

---

**Controller**

- Create Controller

  create controller name:PostController

  php artisan make:controller PostController

  create controller with resource from laravel

  php artisan make:controller --resource PostController

- Passing Data

  add parameter $id, $username, $password in method name

  return view('post')->with('id',$id); or
  return view('post', compact('id', 'username', 'password'));

---

**View**

using .blade.php format

- Setup content:
  import or extends to using the layout or template. layout is folder and app is name of template file (app.blade.php)

        @extends('layout.app')
      start of setup of content of content

        @section('content')

      stop or end of setup of content

        @stop

- Showing of content:

  @yield('content') //show content of content
  @yield('footer') //show content of footer

---

**Migrations**

- Create Migrations
  Create migration name:create_post_table, posts is name of table.

        php artisan make:migration create_post_table --create="posts"

- Delete / Drop table
  Drop all database table migration

        php artisan migrate:reset

- Rollback Migrations
  Rollback the last database migration

        php artisan migrate:rollback

- Status Migrations
  Check the status migration on database

        php artisan migrate:status

- Refresh Migrations
  Reset and re-run all migrations

        php artisan migrate:refresh

- Proccess Migrations to database
  Proccess migrations to database

        php artisan migrate

---

**Laravel Command**
help command by laravel for want you to do

> php artisan

to check the route

> php artisan route:list

create controller name:PostController

> php artisan make:controller PostController

create controller with resource from laravel

> php artisan make:controller --resource PostController
