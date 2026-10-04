# Bitcoin Price Explorer

A small full-stack application that retrieves historical Bitcoin pricing data through a Laravel API and presents it in a Vue.js interface.

## Architecture

- `Backend-laravel/` — Laravel API layer that requests pricing data from the external CoinDesk service
- `frontend-VueJS/` — Vue.js interface for selecting a date range and displaying the returned prices

The frontend calls the Laravel endpoint, which keeps the external API integration behind the application's own REST interface.

## Technology

- PHP and Laravel
- Vue.js and JavaScript
- REST API integration
- Composer and npm

## Run locally

### Backend

```bash
cd Backend-laravel
cp .env.example .env
composer install
php artisan key:generate
php artisan serve
```

### Frontend

```bash
cd frontend-VueJS
npm install
npm run serve
```

Open the frontend URL shown by Vue CLI, select the required date range, and render the result.

## Screenshot

![Bitcoin Price Explorer result](images/Result.png)

> This is an earlier portfolio project retained as a practical example of a Laravel/Vue API integration. Its dependency versions should be upgraded before production use.
