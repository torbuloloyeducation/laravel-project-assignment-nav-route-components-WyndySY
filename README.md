HEAD
[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Y1OyzUvs)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=23353707&assignment_repo_type=AssignmentRepo)
<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

## Project Setup Guide (For Students)

Follow these steps to clone and run the project locally. You are encouraged to explore and modify the code freely.


### 1. Install Dependencies

Install PHP and JavaScript dependencies:

```bash
composer install
npm install
```

### 2. Setup Environment File

Copy the example environment file:

```bash
cp .env.example .env
```

Then open `.env` and configure your database and other settings if needed.

### 3. Generate Application Key

```bash
php artisan key:generate
```

### 4. Run Migrations (if applicable)

```bash
php artisan migrate
```

### 5. Build Frontend Assets

```bash
npm run dev
```

### 6. Run the Application

```bash
php artisan serve
```

Open your browser and go to:

```
http://127.0.0.1:8000
```

---

## Activity 1: Simple Navigation

Your task is to build a very simple navigation system using Laravel.

### Objective

Create a navbar with three links:

* Home
* About
* Contact
* Services
* Showcases
* Blog

Each link should display a simple message when clicked.

### Expected Output

* Home → "Welcome to homepage"
* About → "About us section"
* Contact → "Contact page"
* Services → "Services page"
* Showcases → "Showcases page"
* Blog → "Blog page"

### Steps

1. Create a navbar component inside:

```
resources/views/components/navbar.blade.php
```

Add:

```blade
<nav>
    <a href="/">Home</a> |
    <a href="/about">About</a> |
    <a href="/contact">Contact</a> |
    <a href="/services">Services</a> |
    <a href="/showcases">Showcases</a> |
    <a href="/blog">Blog</a> 
</nav>
<hr>
```

2. Use the navbar in your layout:

```blade
<x-navbar />
{{ $slot }}
```

3. Make sure your routes are defined in `routes/web.php`:

```php
Route::get('/', function () {
    return view('welcome');
}); or Route::view('/', 'welcome');

##both routes above works but view works only for static webpages.

Route::get('/about', function () {
    return view('about');
});

Route::get('/contact', function () {
    return view('contact');
});


...
```

4. Update each page:

**welcome.blade.php**

```blade
<x-layout>
    <h1>Welcome to homepage</h1>
</x-layout>
```

**about.blade.php**

```blade
<x-layout>
    <h1>About us section</h1>
</x-layout>
```

**contact.blade.php**

```blade
<x-layout>
    <h1>Contact page</h1>
</x-layout>
```

```
...
```
---

## Notes for Students

* Feel free to modify the code and experiment.
* Breaking things is part of learning—don’t be afraid to try.
* If something stops working, you can always re-clone the project.
* Make sure your database is properly configured in `.env`.

---

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. It simplifies common tasks like routing, authentication, and database management.

For full documentation, visit: [https://laravel.com/docs](https://laravel.com/docs)

---

## License

This project follows the MIT license.
=======
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

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

In addition, [Laracasts](https://laracasts.com) contains thousands of video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

You can also watch bite-sized lessons with real-world projects on [Laravel Learn](https://laravel.com/learn), where you will be guided through building a Laravel application from scratch while learning PHP fundamentals.

## Agentic Development

Laravel's predictable structure and conventions make it ideal for AI coding agents like Claude Code, Cursor, and GitHub Copilot. Install [Laravel Boost](https://laravel.com/docs/ai) to supercharge your AI workflow:

```bash
composer require laravel/boost --dev

php artisan boost:install
```

Boost provides your agent 15+ tools and skills that help agents build Laravel applications while following best practices.

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
 609f145 (Initial commit for Laravel activity)
