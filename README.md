# Laravel 5.6 + Quasar Framework 0.15 (PWA)

## Build Setup
> rename or copy  .env.example to .env

``` bash
# install php dependencies
$ composer install

# Node.js >= 8.9.0 is required.
$ npm install -g quasar-cli

# install node dependencies
$ npm install

# generate key
$ artisan key:generate

# set privileges to node_modules folder (optional)
#$ chmod -R u+x node_modules/

# first serve the backend (in another console tab, don't use the artisan's serve url in this mode)
$ artisan serve

# then build for development mode
$ quasar dev -m pwa

# OR

# build for production (it'll generate the necessary files, static
# resources and the service-worker)
$ quasar build -m pwa
```

## Laravel License
The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

## Quasar License
Copyright (c) 2016-2017 Razvan Stoenescu
[MIT License](http://en.wikipedia.org/wiki/MIT_License)
