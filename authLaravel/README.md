
Installation Laravel Jestream 

Installation 

> (concurrently) npm i concurrently -g 

(update scripts package json) 
 "start": "concurrently  \"php artisan config:cache\" \"php artisan serve\" \"npm run dev \"  "
