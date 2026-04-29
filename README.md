# HelpIT

HelpIT is an internal helpdesk and ticketing system designed to manage support requests, incidents, and operational workflows efficiently.

## Overview

HelpIT is a customized version of an open-source helpdesk platform, tailored for internal company use. It centralizes issue tracking, improves response time, and streamlines support processes.

## Features

- Ticket management system
- User and role-based access control
- Internal support tracking
- Dashboard and reporting
- Notification and email support
- Customizable workflows

## Tech Stack

- PHP (Laravel Framework)
- MySQL Database
- Nginx (Reverse Proxy)
- Docker (Containerized Deployment)

## Requirements

- PHP 8.1+
- MySQL 8.0+ or MariaDB 10.6+
- Web Server (Nginx / Apache)
- Required PHP Extensions:
  - Mbstring
  - OpenSSL
  - PDO
  - XML
  - Zip

## Installation (Docker)

1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/HelpIT.git
cd HelpIT
```

2. Build and run containers:
```bash
docker compose up -d --build
```

3. Setup environment:

If `.env` exists, edit it.  
If not, create one manually.

4. Generate application key:
```bash
docker exec -it helpit_app php artisan key:generate
```

5. Access the system:
```
http://YOUR_SERVER_IP/helpit
```

## Deployment

HelpIT runs inside Docker containers and is served through an Nginx reverse proxy setup.

## Notes

- Ensure correct permissions for:
  - `storage`
  - `bootstrap/cache`
- Configure `.env` properly before running the app
- Use reverse proxy for cleaner URL access

## Credits

This project is based on the open-source Faveo Helpdesk system and Laravel framework.

## License

This project follows the original open-source license included in the repository. Refer to the LICENSE file for details.
