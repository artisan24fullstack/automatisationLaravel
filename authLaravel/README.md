
## Installation Laravel Jestream 

[Jestream](https://jetstream.laravel.com/installation.html)

> composer require laravel/jetstream

### Install Jetstream With Livewire ​

> php artisan jetstream:install livewire

### Finalizing the Installation ​
 > npm install
 > php artisan migrate

## Installation (concurrently)

>  npm i concurrently -g 

(update scripts package json) 
 "start": "concurrently  \"php artisan config:cache\" \"php artisan serve\" \"npm run dev \"  "

## Installation (Livewire)

[livewire](https://livewire.laravel.com/docs/quickstart)


> composer require livewire/livewire

> php artisan livewire:publish --assets

```
INFO  Publishing [livewire:assets] assets.
```

## Create a Livewire component

> php artisan make:livewire counter

- This command will generate two new files in your project:

- app/Livewire/Counter.php
- resources/views/livewire/counter.blade.php

```
 COMPONENT CREATED  

CLASS: app/Livewire//Counter.php
VIEW:  \resources\views/livewire/counter.blade.php

  _._
/ /o\ \   || ()                ()  __
|_\ /_|   || || \\// /_\ \\ // || |~~ /_\
 |`|`|    || ||  \/  \\_  \^/  || ||  \\_


Congratulations, you've created your first Livewire component!
```
### Writing the class

- Open app/Livewire/Counter.php and replace its contents with the following:

### Writing the view
- Open the resources/views/livewire/counter.blade.php file and replace its content with the following:


### Register a route for the component
- Open the routes/web.php file in your Laravel application and add the following code:

### Create a template layout

> php artisan livewire:layout

# Test it out
- With our component class and templates in place, our component is ready to test!

> Visit /counter in your browser
