![Packagist Version](https://img.shields.io/packagist/v/ultrono/laravel-sitemap)
[![run-tests-laravel-8-9](https://github.com/ultrono/laravel-sitemap/actions/workflows/workflow.yml/badge.svg)](https://github.com/ultrono/laravel-sitemap/actions/workflows/workflow.yml)
[![PHP ^8.0](https://img.shields.io/badge/php-%5E8.0-green)]()

# Laravel Sitemap

This is a `PHP ^8.0` Laravel 8 and 9 only fork of [Laravelium/laravel-sitemap](https://github.com/Laravelium/laravel-sitemap), as the original repository has been abandoned and does not support Laravel 9.

**Support for < 8 or PHP 8 have been dropped**.

## Installation

```bash
composer require ultrono/laravel-sitemap
```

```bash
php artisan vendor:publish --provider="Ultrono\Sitemap\SitemapServiceProvider"
```

## Generate a simple sitemap

```php
Route::get('mysitemap', function() {
    $sitemap = resolve("sitemap");

    $sitemap->add(URL::to(), '2012-08-25T20:10:00+02:00', '1.0', 'daily');
    $sitemap->add(URL::to('page'), '2012-08-26T12:30:00+02:00', '0.9', 'monthly');

    $posts = DB::table('posts')->orderBy('created_at', 'desc')->get();

    foreach ($posts as $post) {
        $sitemap->add($post->slug, $post->modified, $post->priority, $post->freq);
    }

    // generate (format, filename)
    // sitemap.xml is stored within the public folder
    $sitemap->store('xml', 'sitemap');
});
```

## Examples

- [How to generate dynamic sitemap (with optional caching)](https://web.archive.org/web/20201130155031/https://github.com/Laravelium/laravel-sitemap/wiki/Dynamic-sitemap)
- 

- [How to generate BIG sitemaps (with more than 1M items)](https://web.archive.org/web/20201130155031/https://github.com/Laravelium/laravel-sitemap/wiki/Sitemap-index)

- [How to generate sitemap to a file](https://web.archive.org/web/20201130155030/https://github.com/Laravelium/laravel-sitemap/wiki/Generate-sitemap)

- [How to use multiple sitemaps with sitemap index](https://web.archive.org/web/20201130155030/https://github.com/Laravelium/laravel-sitemap/wiki/Generate-BIG-sitemaps)

and more in the [Wiki](https://web.archive.org/web/20201130155038/https://github.com/Laravelium/laravel-sitemap/wiki).
