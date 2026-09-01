# Laravel Query Website

A Laravel-based web scraping application that automatically fetches vehicle inventory data from the Quest MultiMarcas website and stores it in a MySQL database for analysis and monitoring.

The application is designed to:

- Make HTTP requests to the Quest MultiMarcas vehicle inventory website
- Extract and parse vehicle data from search results
- Store vehicle information in a MySQL database
- Provide a structured Laravel framework for data management
- Enable vehicle availability monitoring and inventory tracking

## Features

- Automated web scraping of vehicle inventory data
- HTTP request handling with data extraction
- MySQL database integration for persistent data storage
- Laravel framework structure for scalability and maintainability
- Vehicle data parsing and normalization
- Inventory aggregation from dealership website
- Easy-to-extend architecture for additional data fields

## Requirements

- **PHP** 7.4 or higher
- **Laravel Framework** 7.28.4 or compatible version
- **Composer** 2.1
- **MySQL** database server
- **Node.js** (optional, for frontend assets)

## Installation

1. **Clone or download the project**
```text
git clone https://github.com/MaiaMayCry/laravel\_query\_website.git
cd laravel_query_website
```

2. **Install dependencies**
```text
composer install
```

3. **Set up environment configuration**
- Copy `.env.example` to `.env`
- Configure your MySQL database credentials in the `.env` file
```text
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database_name
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

4. **Generate application key**
```text
php artisan key:generate
```

5. **Run database migrations**
```text
php artisan migrate
```

## Usage

1. **Configure the scraping target**
- Update the website URL in the scraping configuration

2. **Execute the scraper**
- Run the artisan command to fetch and store vehicle data
```text
php artisan scrape:vehicles
```

3. **Monitor the database**
- Vehicle data is stored in MySQL and accessible through the Laravel application

4. **Query the data**
- Use Laravel Eloquent models to retrieve and analyze vehicle information

## Notes

- Ensure you have proper permissions to scrape the target website
- Schedule regular scraping tasks using Laravel's task scheduler if needed
- Monitor database growth and implement data cleanup policies as appropriate
