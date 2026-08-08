# Stockroom

Stockroom is a Django inventory and sales management MVP for small teams. It tracks products, categories, stock levels, and sales in a responsive business workspace.

## Run & Operate

- `cd inventory_sales_manager && python manage.py runserver` — run the Django app locally
- `cd inventory_sales_manager && python manage.py migrate` — apply SQLite migrations
- `cd inventory_sales_manager && python manage.py seed_data` — create demo records
- The Replit preview runs through the `Inventory Sales Manager` workflow on port 8000.

## Stack

- Python 3, Django, SQLite, Django ORM
- HTML5, CSS3, Bootstrap 5, Chart.js
- Django built-in authentication

## Where things live

- `inventory_sales_manager/config/` — Django settings, URLs, and WSGI entry point
- `inventory_sales_manager/inventory/` — categories, products, forms, dashboard, admin, and seed command
- `inventory_sales_manager/sales/` — sales model, transactional stock reduction, forms, views, and admin
- `inventory_sales_manager/templates/` — authenticated workspace, auth pages, and responsive UI templates
- `inventory_sales_manager/static/css/app.css` — shared visual theme
- `inventory_sales_manager/README.md` — setup, demo credentials, and feature overview

## Architecture decisions

- SQLite is the source of truth for this MVP, keeping setup portable and dependency-light.
- Sale creation uses a database transaction and row locking before reducing inventory.
- The dashboard derives revenue, stock, and activity values from live database queries.
- Django templates and Bootstrap keep the UI easy to extend without a separate frontend build.

## Product

- Authenticated staff can review live business metrics, manage products and categories, and record sales.
- Product SKUs are unique and low-stock thresholds surface items that need attention.
- Sales store the creating user, preserve the selling price, and automatically reduce stock.

## User preferences

- Keep the app focused on the requested inventory and sales MVP; avoid adding infrastructure or services unless requested.

## Gotchas

- Run `makemigrations` when model fields change, then `migrate`; use `seed_data` for repeatable demo data.

## Pointers

- `inventory_sales_manager/README.md` contains the full setup and demo instructions.