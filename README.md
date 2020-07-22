# Index pages in Google

**WORK IN PROGRESS, some functionalities may be changed in the future.**

Request a page to be indexed by Google using the [Indexing API](https://developers.google.com/search/apis/indexing-api/v3/quickstart).

Please, take a note at the allowed pages that can be index using this API at https://developers.google.com/search/apis/indexing-api/v3/quickstart.

## Installation

You can install the package via composer:

```bash
composer require risingsun/laravel-google-indexing
```

Next you have to follow the setup instructions from Google, this can be found here [Google Indexing API documentation](https://developers.google.com/search/apis/indexing-api/v3/prereqs).

You need to make a file in your storage direct, but you can override this setting in config with the key `laravel-google-indexing.google.auth_config`.

> Soon we'll publish a blog post on how to setup this package. 

## Usage

> NOTE: this package works only for verified sites in your Google Search Console account

Inform Google about a new or updated URL:
```php
LaravelGoogleIndexing::create()->update('https://www.my-domain.com')
```

Delete an URL from the index:
```php
LaravelGoogleIndexing::create()->delete('https://www.my-domain.com')
```

Get the status of an URL:
``` php
LaravelGoogleIndexing::create()->status('https://www.my-domain.com')
```

##Or use the Facade
Inform Google about a new or updated URL:
```php
LaravelGoogleIndexing::update('https://www.my-domain.com')
```

Delete an URL from the index:
```php
LaravelGoogleIndexing::delete('https://www.my-domain.com')
```

Get the status of an URL:
``` php
LaravelGoogleIndexing::status('https://www.my-domain.com')
```

### Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information on what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

### Security

If you discover any security related issues, please email gaoxu529@126.com instead of using the issue tracker.

## Credits

- [Robin Dirksen](https://github.com/gaoxu529) ([personal site](https://www.bjestrata.com))
- [risingsun](https://www.bjestrata.com)
- [All Contributors](../../contributors)

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
