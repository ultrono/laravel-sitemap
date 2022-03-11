[![run-tests-laravel-8-9](https://github.com/ultrono/laravel-sitemap/actions/workflows/workflow.yml/badge.svg)](https://github.com/ultrono/laravel-sitemap/actions/workflows/workflow.yml)
[![PHP ^8.0](https://img.shields.io/badge/php-%5E8.0-green)]()

# Laravel Sitemap

This is a `PHP ^8.0` Laravel 8 and 9 only fork of [Laravelium/laravel-sitemap](https://github.com/Laravelium/laravel-sitemap), as the original repository has been abandoned and does not support Laravel 9.

**Support for < 8 or PHP 8 have been dropped**.

## Installation

Run the following command and provide the latest stable version (e.g v8.\*) :

```bash
composer require ultrono/laravel-sitemap
```


Optionally publish assets (styles, views, config files):

```bash
php artisan vendor:publish --provider="Laravelium\Sitemap\SitemapServiceProvider"
```

## Examples

- [How to generate dynamic sitemap (with optional caching)](https://github.com/Laravelium/laravel-sitemap/wiki/Dynamic-sitemap)

- [How to generate BIG sitemaps (with more than 1M items)](https://github.com/Laravelium/laravel-sitemap/wiki/Sitemap-index)

- [How to generate sitemap to a file](https://github.com/Laravelium/laravel-sitemap/wiki/Generate-sitemap)

- [How to use multiple sitemaps with sitemap index](https://github.com/Laravelium/laravel-sitemap/wiki/Generate-BIG-sitemaps)

and more in the [Wiki](https://github.com/Laravelium/laravel-sitemap/wiki).
