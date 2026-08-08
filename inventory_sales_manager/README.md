# Stockroom

Stockroom is a polished inventory and sales management MVP built for small teams. It keeps product stock, categories, sales history, and business health in one simple workspace.

## Features

- Built-in Django authentication with registration, login, and protected workspace pages
- Dashboard with live stock totals, low-stock alerts, revenue stats, recent sales, and a 7-day Chart.js overview
- Product CRUD with unique SKUs, categories, search, filtering, low-stock thresholds, and delete confirmation
- Category management
- Sales recording with transactional stock reduction, automatic pricing, and insufficient-stock validation
- Useful Django admin configuration for products, categories, and sales
- Seed command with demo categories, eight products, sample sales, and a demo user
- Responsive Bootstrap 5 interface with a focused business dashboard design

## Tech stack

Python 3 · Django · SQLite · Django ORM · HTML5 · CSS3 · Bootstrap 5 · Chart.js

## Installation

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py seed_data
python manage.py runserver
```

Create an administrator with:

```bash
python manage.py createsuperuser
```

Open `http://127.0.0.1:8000/`. In Replit, use the running **Inventory Sales Manager** preview.

## Demo credentials

After running `seed_data`:

- Username: `demo`
- Password: `demo12345`

## Screenshots

_Add screenshots of the dashboard, catalog, and sales history here._

## Future improvements

- CSV export for products and sales
- Supplier and purchase-order tracking
- Granular team permissions
- Barcode scanning
- Automated low-stock notifications