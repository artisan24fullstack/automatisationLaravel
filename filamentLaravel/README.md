
## Mise en place (model & migration)

> php artisan make:model Post -m -c -f

```
   INFO  Model [\app\Models\Post.php] created successfully.  

   INFO  Factory [\database\factories\PostFactory.php] created successfully.  

   INFO  Migration [\database\migrations/2024_07_05_082550_create_posts_table.php] created successfully.
```

> php artisan make:model Category -m -f

```
   INFO  Model [\app\Models\Category.php] created successfully.

   INFO  Factory [\database\factories\CategoryFactory.php] created successfully.

   INFO  Migration [\database\migrations/2024_07_05_082602_create_categories_table.php] created successfully.
```

> php artisan make:migration create_category_post_table

```
   INFO  Migration [\database\migrations/2024_07_05_082624_create_category_post_table.php] created successfully.
```

## Installation Concurrently 

> npm i concurrently -g

```
        "start": "concurrently  \"php artisan config:cache\" \"php artisan serve\" \"npm run dev \"  "
```

## Installation Filament 

[Filament](https://filamentphp.com/docs/3.x/panels/installation)

[Demo Filament](https://demo.filamentphp.com/login)

> composer require filament/filament:"^3.0"

> php artisan filament:install --panels

> php artisan migrate

```
   WARN  The SQLite database does not exist:\database\database.sqlite.

  Would you like to create it? (yes/no) [no]
❯ yes

   INFO  Preparing database.

  Creating migration table ............................................................................................................... 11ms DONE

   INFO  Running migrations.

  2014_10_12_000000_create_users_table ................................................................................................... 10ms DONE
  2014_10_12_100000_create_password_reset_tokens_table .................................................................................... 4ms DONE
  2019_08_19_000000_create_failed_jobs_table .............................................................................................. 9ms DONE
  2019_12_14_000001_create_personal_access_tokens_table .................................................................................. 12ms DONE
  2024_07_05_082550_create_posts_table .................................................................................................... 9ms DONE
  2024_07_05_082602_create_categories_table ............................................................................................... 8ms DONE
  2024_07_05_082624_create_category_post_table ............................................................................................ 5ms DONE
```

## Create a user (admin)

> php artisan make:filament-user
```
 Name:
 Email address:
 Password:

   INFO  Success! (email adresse) may now log in at http://localhost:8000/admin/login.
```

> php artisan make:filament-resource Category

```
   INFO  Successfully created CategoryResource!
```

> php artisan make:filament-resource Post --soft-deletes

```
   INFO  Successfully created PostResource!
```

> php artisan make:filament-resource User --generate

```   
   INFO  Successfully created UserResource!
```

> php artisan vendor:publish --tag=filament-config

```
   INFO  Publishing [filament-config] assets.  

  Copying file [\vendor\filament\support\config\filament.php] to [\filamentLaravel\config\filament.php]  DONE
```

> php artisan storage:link

```
   INFO  The [\filamentLaravel\public\storage] link has been connected to [\filamentLaravel\storage\app/public].
```
