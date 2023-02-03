## Redeem Ticket System

This is a system to redeem tickets for events. Features of this system include
- Ticket redemption
- Rate limiting system on how many tickets can be redeemed per hour

### Tech Stack
- PHP 8.1
- Laravel
- Composer
- Postgresql
- Redis
- Docker Compose (Laravel Sail)
- Scout APM - for monitoring

### Prerequisites
- [Docker with docker compose](https://www.docker.com/).
- [Git](https://git-scm.com/) - to clone repository (optional)
- [PHP 8.1](https://php.net) must be installed on the command line

### How to set up
- Clone the repository to your computer from your terminal using `git clone https://github.com/brytey2k/redeem-ticket-system.git` or download the repository
- Run `cp .env.example .env` from your command line to create the system environment configuration file
- Open `.env` file with your favourite editor and insert the correct configurations.
- Create database giving it the same name specified in `.env` file
- Run `composer install`
  - You may see a `Predis\Connection\ConnectionException` exception but this is because laravel has not been started yet. We start laravel sail in the next step
- Run `./vendor/bin/sail up -d` to start up the application
- Run `sail artisan migrate --seed` to create the database with initial data for testing
- System can accessed at http://laravel.test
- Use email: admin@admin.com and password: password to login

## Tests
To run tests, run `sail artisan test`

## Security Vulnerabilities

If you discover a security vulnerability within this system, please send an e-mail to Bright Nkrumah via [brytey2k@gmail.com](mailto:brytey2k@gmail.com). All security vulnerabilities will be promptly addressed.
