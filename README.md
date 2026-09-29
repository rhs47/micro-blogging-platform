# Laravel MVC micro blogging platform

Chirper is a small Laravel application for sharing short posts (“chirps”). Visitors can browse the latest posts, create an account, and sign in. Signed-in users can publish chirps of up to 255 characters and edit or delete their own posts.

## Features

- Public feed showing the 50 most recent chirps
- Account registration, sign-in, and sign-out
- Create, edit, and delete chirps while signed in
- Authorization that limits editing and deletion to the chirp’s author
- Responsive Blade interface styled with Tailwind CSS and daisyUI

## Tech stack

- PHP 8.3 or newer
- Laravel 13
- SQLite by default (database settings can be changed in `.env`)
- Blade templates
- Vite, Tailwind CSS 4, and daisyUI 5
- Pest for automated tests

## Getting started

You’ll need PHP, Composer, Node.js, and npm installed.

1. Clone the repository and enter the project directory.
2. Install dependencies, create the local environment file and application key, migrate the database, and build frontend assets:

```bash
   composer run setup
```

3. Start the Laravel application and Vite development server:

```bash
   composer run dev
```

Open the local URL printed by Laravel’s development server. New users can register from the **Sign Up** link.

To run the test suite:

```bash
composer run test
```

## Project structure

- `app/Models` — User and Chirp Eloquent models
- `app/Http/Controllers` — Chirp and authentication request handling
- `app/Policies` — Chirp ownership authorization
- `routes/web.php` — Web routes
- `resources/views` — Blade pages and reusable components
- `database/migrations` — Database schema
- `tests` — Pest feature and unit tests
