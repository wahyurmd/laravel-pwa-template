<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Laravel (PWA) Progressive Web Aplication

[![Laravel 7.x](https://img.shields.io/badge/Laravel-7.x-red.svg)](https://laravel.com)
[![Laravel 8.x](https://img.shields.io/badge/Laravel-8.x-red.svg)](https://laravel.com)
[![Laravel 9.x](https://img.shields.io/badge/Laravel-9.x-red.svg)](https://laravel.com)
[![Laravel 10.x](https://img.shields.io/badge/Laravel-10.x-red.svg)](https://laravel.com)

This Laravel pakage turns your project into a [progressive web app](https://developers.google.com/web/progressive-web-apps/).  Navigating to your site on an Android phone will prompt you to add the app to your home screen.

Launching the app from your home screen will display your app.  As such, it's critical that your application provides all navigation within the HTML (no reliance on the browser back or forward button).

Requirements
=====
Progressive Web Apps require HTTPS unless being served from localhost.  If you're not already using HTTPS on your site, check out [Let's Encrypt](https://letsencrypt.org/) and [ZeroSSL](https://zerossl.com/).

## use of PWA

1. Adjust the `logo.png` in the "public" folder, change it with your logo.
2. Add the following code inside the head tag of your main file:
```php
<meta name="theme-color" content="#6777ef"/>
<link rel="apple-touch-icon" href="{{ asset('logo.PNG') }}">
<link rel="manifest" href="{{ asset('manifest.json') }}">
```
3. Also add the code below before closing the body tag in your main file:
```php
<script src="{{ asset('sw.js') }}"></script>
<script>
    if (!navigator.serviceWorker.controller) {
        navigator.serviceWorker.register("/sw.js").
        then(function (reg) {
            console.log("Service worker has been registered for scope: " + reg.scope);
        });
    }
</script>
```
