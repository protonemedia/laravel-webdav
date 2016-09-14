# laravel-webdav

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Software License][ico-license]](LICENSE.md)
[![Total Downloads][ico-downloads]][link-downloads]

## Install

Via Composer

``` bash
$ composer require pbmedia/laravel-webdav
```

## Usage

Register the service provider in your app.php config file:

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
	    'driver'   => 'webdav',
	    'baseUri'  => env('WEBDAV_HOST', 'https://mywebdavstorage.com',
	    'userName' => env('WEBDAV_USERNAME', 'jdoe'),
	    'password' => env('WEBDAV_PASSWORD', ''),
	],
	...
];
```

## Change log

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) and [CONDUCT](CONDUCT.md) for details.

## Security

If you discover any security related issues, please email info@pascalbaljetmedia.com instead of using the issue tracker.

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
