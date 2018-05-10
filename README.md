# seedster
Register laravel seeds from a package

# Installation
require the project using Composer:
```
composer require eklundkristoffer/seedster
```
or manually update your require block and run composer update
```
{
    "require": {
        "eklundkristoffer/seedster": "^3.0"
    }
}
```
and finally add `Seedster\SeedsterServiceProvider::class` to your `providers` array.

# Usage
You can now register a seed from any service provider
```php
use Mypackage\Database\Seeds\UserTableSeeder;

public function register()
{
    $this->app['seed.handler']->register(
        UserTableSeeder::class
    );
}
```
