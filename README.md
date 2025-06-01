# Laravel CRUD Application

A basic CRUD (Create, Read, Update, Delete) application built with Laravel 12, featuring Category and Post management with relationships.

## Features
- **Category Management**: Full CRUD operations for categories
- **Post Management**: Full CRUD operations for blog posts
- **Relationships**: Posts belong to categories (one-to-many relationship)
- **Validation**: Form validation for all inputs
- **UI**: Responsive Bootstrap interface

## Requirements
- PHP 8.1+
- Composer
- MySQL 8.0+
- Node.js 18+ (for frontend dependencies)

## Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/TannyCoder/CRUD-App-Laravel-12
cd laravel-crud-app
```

### 2. Install dependencies
```bash
composer install
npm install
```
### 3. Configure environment
# 1. Copy .env.example to .env:
```bash
cp .env.example .env
```
# 2. Generate app key:
```bash
php artisan key:generate
```
# 3. Update database credentials in .env:
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=cms_new
DB_USERNAME=root
DB_PASSWORD=

### 4. Run migrations and seeders
```bash
php artisan migrate --seed
```
### 5. Build frontend assets
```bash
npm run build
```
### 6. Start development server
```bash
php artisan serve
```

Usage Guide
Category Management
List Categories: /categories
View all categories

Create Category: /categories/create
Add new categories

Edit Category: /categories/{id}/edit
Modify existing categories

Delete Category: Click delete button
Remove categories (with confirmation)

Post Management
List Posts: /posts
View all posts with pagination

Create Post: /posts/create
Add new blog posts (select category from dropdown)

View Post: /posts/{id}
See post details

Edit Post: /posts/{id}/edit
Modify existing posts

Delete Post: Click delete button
Remove posts (with confirmation)

Relationships
Each post belongs to a category

Categories show post counts

Filter posts by category

# Project structure
app/
├── Models/
│   ├── Category.php
│   └── Post.php
├── Http/
│   ├── Controllers/
│   │   ├── CategoryController.php
│   │   └── PostController.php
database/
├── migrations/
│   ├── create_categories_table.php
│   └── create_posts_table.php
├── seeders/
│   └── DatabaseSeeder.php
resources/
├── views/
│   ├── categories/
│   └── posts/
routes/
└── web.php

Seeded Test Data
The database seeder creates:
1 admin user:
Email: tankyaaah@gmail.com
Password: tankyaaah@gmail.com

# Troubleshooting
Migration errors: Run php artisan migrate:fresh --seed
Class not found: Run composer dump-autoload
Assets not loading: Run npm run build
Permission issues: Run chmod -R 775 storage bootstrap/cache
