# PHP Laravel Docker Boilerplate

A Docker-based development environment boilerplate for PHP and Laravel applications. This project provides a pre-configured, containerized setup that allows developers to quickly spin up a complete PHP development environment with all necessary services.

## Tech Stack

- **PHP 8.2** - PHP-FPM Alpine image with PDO MySQL extensions
- **Nginx** - Stable Alpine image used as a reverse proxy and web server
- **MySQL 5.7** - Relational database for data persistence
- **phpMyAdmin** - Web-based database management interface
- **Docker & Docker Compose** - Container orchestration

## Project Structure

```
.
├── docker-compose.yml      # Docker Compose configuration
├── dockerfiles/
│   └── php.dockerfile      # PHP container configuration
├── nginx/
│   └── nginx.conf          # Nginx server configuration
├── public/
│   └── index.php           # Application entry point
└── env/
    └── mysql.env           # MySQL environment variables
```

## Services

| Service     | Port  | Description                          |
|-------------|-------|--------------------------------------|
| Nginx       | 8001  | Web server                           |
| MySQL       | 3306  | Database server                      |
| phpMyAdmin  | 8180  | Database management UI               |
| PHP-FPM     | 9000  | PHP FastCGI Process Manager (internal) |

## Getting Started

### Prerequisites

- Docker
- Docker Compose

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/raiyan24r/php-laravel-docker-boilerplate.git
   cd php-laravel-docker-boilerplate
   ```

2. Start the containers:
   ```bash
   docker-compose up -d
   ```

3. Access the application:
   - Web application: http://localhost:8001
   - phpMyAdmin: http://localhost:8180

### Database Configuration

Default MySQL credentials (configured in `env/mysql.env`):
- Database: `homestead`
- User: `homestead`
- Password: `secret`
- Root Password: `secret`

## Usage

Place your Laravel or PHP application files in the project root. The `public/` directory serves as the web root for Nginx.

## Stopping the Environment

```bash
docker-compose down
```

## License

This project is open-source and available for use in your own projects.
