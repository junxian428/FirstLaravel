# FirstLaravel

Laravel PHP framework 
1. Learning Website

https://youtu.be/ImtZ5yENzgE




Debug
_______________________________________________________________________________________________
Issues:

1.php artisan make:auth  (not longer supported)

Solution：

php artisan ui:auth

2. npm run development

Compilation error.
Notification Error.

Add this line in webpack

mix.disableNotifications();

https://medium.com/@irsyadadl/how-i-turn-off-the-notification-laravel-mix-build-successful-81463cbe2ae6




___________________________________________________________________________________
### FIX ISSUES ###
FIX/TIP (4:15) - echo $PATH does not work under windows (prompt). Instead, you must try just "path" (remove the quotations) on cmd/prompt.

FIX (9:38) - ERROR "Could not open input file: artisan" when run "php artisan serve": As he said, we must run this command inside the project folder. 

FIX (11:45) - make:auth works only on Laravel 5.8 and older versions.* The newer version, try: 
1. composer require laravel/ui
2. php artisan ui vue --auth
3. npm install && npm run dev

FIX (22:00) - If you try to use "vim" over Windows cmd: for Windows users, "vim" should not works. So, being at the project folder, try: copy con database\database.sqlite (press enter, so F6 then, enter again). It will create the file with nothing inside. METHOD 2: re-create this file using a different method, like (under windows os) right-click on the project folder, "create new text file" (but rename the extension txt to sqlite!) and rename it to database.sqlite

FIX (23:35) - console echoes for php artisan migrate: "Could not find driver (SQL: PRAGMA...": Just open php.ini and uncomment extension=pdo_sqlite (or extension=pdo_mysql if you use it).
If this error persists, even after uncommenting  extension=pdo_sqlite, with PHP Warning "PHP Startup: Unable to load dynamic library 'pdo_sqlite'". Try fix that by typing: 
sudo apt-get install php7.4-sqlite
(Thanks to @Sjors Peterse)


Learning Resources: https://youtu.be/ImtZ5yENzgE
