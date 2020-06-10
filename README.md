# Run the Laravel scheduler without relying on cron

[![Latest Version on Packagist](https://img.shields.io/packagist/v/spatie/laravel-cronless-schedule.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-cronless-schedule)
[![GitHub Tests Action Status](https://img.shields.io/github/workflow/status/spatie/laravel-cronless-schedule/run-tests?label=tests)](https://github.com/spatie/laravel-cronless-schedule/actions?query=workflow%3Arun-tests+branch%3Amaster)
[![Total Downloads](https://img.shields.io/packagist/dt/spatie/laravel-cronless-schedule.svg?style=flat-square)](https://packagist.org/packages/spatie/laravel-cronless-schedule)

[Laravel's native scheduler](https://laravel.com/docs/master/scheduling) relies on cron to be executed every minute. It's rock sold an in most cases you should stick to using it.

If you want to simulate the scheduler running every minute in a test environment, using cron can be cumbersome. This package provides a command to run the scheduler every minute, without relying on cron. Instead it uses a [ReactPHP](https://reactphp.org) loop.

This is how you can start the cronless schedule:

```bash
php artisan cronless-schedule:run
```

This command will never end. Behind the scenes it will execute `php artisan schedule` every minute. 
 
## Support us

Learn how to create a package like this one, by watching our premium video course:

[![Laravel Package training](https://spatie.be/github/package-training.jpg)](https://laravelpackage.training)

We invest a lot of resources into creating [best in class open source packages](https://spatie.be/open-source). You can support us by [buying one of our paid products](https://spatie.be/open-source/support-us).

We highly appreciate you sending us a postcard from your hometown, mentioning which of our package(s) you are using. You'll find our address on [our contact page](https://spatie.be/about-us). We publish all received postcards on [our virtual postcard wall](https://spatie.be/open-source/postcards).

## Installation

You can install the package via composer. Probably you only want to use this schedule in a development environment.

```bash
composer require spatie/laravel-cronless-schedule --dev
```

## Usage

This is how you can start the cronless schedule:

```bash
php artisan cronless-schedule:run
```

By default, it will run every minute. 

To perform an extra run of the scheduler, just press enter.

If you want to run the scheduler at another frequency, just can pass an amount of seconds to the `frequency` option. Here is an example where the schedule will be run every 5 seconds.

```bash
php artisan cronless-schedule:run --frequency=5
```


## Testing

``` bash
composer test
```

## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Security

If you discover any security related issues, please email freek@spatie.be instead of using the issue tracker.

## Credits

- [Freek Van der Herten](https://github.com/freekmurze)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
