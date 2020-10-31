# laravel-webdav

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Build Status](https://img.shields.io/travis/protonemedia/laravel-webdav/master.svg?style=flat-square)](https://travis-ci.org/protonemedia/laravel-webdav)
[![Software License][ico-license]](LICENSE.md)
[![Total Downloads][ico-downloads]][link-downloads]

This package provides a WebDAV driver for Laravel's Filesystem. Laravel 6.0 and higher supported.

## Install

Via Composer

``` bash
$ composer require pbmedia/laravel-webdav
```

## Usage

Register the service provider in your app.php config file (Laravel 5.4 and lower only):

``` php
// config/app.php

'providers' => [
    ...
    Pbmedia\FilesystemProviders\WebDAVServiceProvider::class
    ...
];
```

Create a webdav filesystem disk:

``` php
// config/filesystems.php

'disks' => [
	...
	'webdav' => [
	    'driver'     => 'webdav',
	    'baseUri'    => 'https://mywebdavstorage.com',
	    'userName'   => 'protonemedia',
	    'password'   => 'supersecretpassword',
	    'pathPrefix' => 'backups', // optional
	],
	...
];
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email info@protone.media instead of using the issue tracker.

## Other Laravel packages

* [`Laravel Analytics Event Tracking`](https://github.com/protonemedia/laravel-analytics-event-tracking): Laravel package to easily send events to Google Analytics.
* [`Laravel Blade On Demand`](https://github.com/protonemedia/laravel-blade-on-demand): Laravel package to compile Blade templates in memory.
* [`Laravel Cross Eloquent Search`](https://github.com/protonemedia/laravel-cross-eloquent-search): Laravel package to search through multiple Eloquent models.
* [`Laravel Form Components`](https://github.com/protonemedia/laravel-form-components): Blade components to rapidly build forms with Tailwind CSS Custom Forms and Bootstrap 4. Supports validation, model binding, default values, translations, includes default vendor styling and fully customizable!
* [`Laravel FFMpeg`](https://github.com/protonemedia/laravel-ffmpeg): This package provides an integration with FFmpeg for Laravel. The storage of the files is handled by Laravel's Filesystem.
* [`Laravel Paddle`](https://github.com/protonemedia/laravel-paddle): Paddle.com API integration for Laravel with support for webhooks/events.
* [`Laravel Verify New Email`](https://github.com/protonemedia/laravel-verify-new-email): This package adds support for verifying new email addresses: when a user updates its email address, it won't replace the old one until the new one is verified.

## Credits

- [Pascal Baljet][link-author]
- [All Contributors][link-contributors]

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/pbmedia/laravel-webdav.svg?style=flat-square
[ico-license]: https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/pbmedia/laravel-webdav.svg?style=flat-square

[link-packagist]: https://packagist.org/packages/pbmedia/laravel-webdav
[link-downloads]: https://packagist.org/packages/pbmedia/laravel-webdav
[link-author]: https://github.com/pascalbaljet
[link-contributors]: ../../contributors
