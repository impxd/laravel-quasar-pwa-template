# Laravel 5.5 + Quasar Framework (PWA)

## Build Setup
> rename or copy  .env.example to .env

``` bash
# install php dependencies
$ composer install

# install node dependencies
$ npm install

# generate key
$ artisan key:generate

# set privileges to node_modules folder (optional)
#$ chmod -R u+x node_modules/

# serve the backend (in another console tab)
$ artisan serve

# build for development mode (don't use the artisan serve url in this mode)
$ npm run dev

# OR

# build for production (it'll generate the necessary laravel files, static
# resources and the service-worker; now you can access through artisan serve)
$ npm run build
```

## Laravel License
The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

## Quasar License
Copyright (c) 2016-2017 Razvan Stoenescu
[MIT License](http://en.wikipedia.org/wiki/MIT_License)
