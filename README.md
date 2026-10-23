# Marktplaats

An online advertising platform built with Laravel, made for the Codebook Laravel chapter (assignment 21). Users can register, place ads in categories, bid on other users' ads and send each other messages.

## Tech stack

- **Laravel 13** with Blade templates
- **Tailwind CSS** via Vite
- **SQLite** database
- **Mailpit** for testing emails locally

Authentication is built by hand on top of Laravel's auth features. No starter kits (Breeze, Jetstream) are used.

## Requirements

- PHP 8.3+
- Composer
- Node.js + npm
- [Mailpit](https://github.com/axllent/mailpit)

## Installation

```bash
git clone https://github.com/MikaEvW/laravel-marktplaats.git
cd laravel-marktplaats

composer install
npm install
npm run build

cp .env.example .env
php artisan key:generate
php artisan migrate
```

`php artisan migrate` asks to create the SQLite database file if it doesn't exist yet.

## Running the app

Run these in separate terminals:

```bash
php artisan serve
```

```bash
mailpit --listen 127.0.0.1:8025 --smtp 127.0.0.1:1025
```

- App: http://127.0.0.1:8000
- Mailpit (catches all outgoing emails): http://127.0.0.1:8025

During development, `npm run dev` rebuilds the CSS and JS automatically on changes.

## Documentation

### Flowchart

![Flowchart](/docs/flowchart.png)

_Editable source: [flowchart.drawio.svg](/docs/flowchart.drawio.svg)_

### Database design

![Database design](/docs/database.png)

## Features

Progress per user story on the project board:

- [ ] MAR-11453: Registration (with email verification)
- [ ] MAR-11454: Login
- [ ] MAR-11455: Password reset
- [ ] MAR-11456: Place an ad
- [ ] MAR-11457: Overview of own ads
- [ ] MAR-11458: Edit ads
- [ ] MAR-11459: Delete ads
- [ ] MAR-11460: Overview of all ads for visitors
- [ ] MAR-11461: Place bids on ads
- [ ] MAR-11462: Overview of bids per ad
- [ ] MAR-11463: Categorize ads
- [ ] MAR-11464: Filter by category
- [ ] MAR-11465: Pagination
- [ ] MAR-11466: Search by keyword
- [ ] MAR-11467: Messages between users
- [ ] MAR-11468: Email notifications for new messages
- [ ] MAR-11469: Paid ad promotion
