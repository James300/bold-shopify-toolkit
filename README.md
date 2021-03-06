# Bold Shopify Toolkit

[![CircleCI](https://circleci.com/gh/bold-commerce/bold-shopify-toolkit/tree/master.svg?style=svg)](https://circleci.com/gh/bold-commerce/bold-shopify-toolkit/tree/master)

Bold Shopify Toolkit is a Symfony Based Shopify Wrapper that makes it easy to interact with Shopify.

## Getting Started

This package works best with a Dependency Injection Container since there are many dependencies that need to be resolved.

### Prerequisites

To use this package, you will need to bind Models to the following interfaces.

- ShopAccessInfo
- ShopBaseInfo
- ApplicationInfo
- ApiSleeper

An example API Sleeper has been included in this package.

Laravel: (In AppServiceProvider.php)

```
    $this->app->bind(\BoldApps\ShopifyToolkit\Contracts\ApiSleeper::class,
            \BoldApps\ShopifyToolkit\Support\ShopifyApiHandler::class);

```

### Installing

Add to composer.json

```
composer require bold-commerce/bold-shopify-toolkit
```

Bind the appropriate models during your request lifecycle.

```
    $this->app->bind(\BoldApps\ShopifyToolkit\Contracts\ApiSleeper::class,
            \BoldApps\ShopifyToolkit\Support\ShopifyApiHandler::class);

    ...
```

## Running the tests

```
vendor/bin/phpunit tests
```

## TODO

* Add more tests
* Examples

## Contributing

Pull requests and ideas are welcome! Open an issue and lets talk.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/bold-commerce/bold-shopify-toolkit/tags).

## License

This project is licensed under the Apache 2 License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Thanks to Shopify for making the best Developer Network!
* Thanks to Bold Commerce Developers for making this amazing package
