# Advanced Inventory Management System

A comprehensive Flask-based inventory management system designed for managing bus parts, products, categories, and user roles with advanced reporting capabilities.

## Features

- 🔐 **Role-Based Access Control**
  - Admin, Manager, Supervisor, and User roles
  - Different permissions for different roles
  - Secure authentication system

- 📦 **Inventory Management**
  - Product management with categories
  - Low stock alerts
  - Bulk upload capabilities
  - Real-time stock tracking

- 🚌 **Bus Management**
  - Detailed bus information tracking
  - Parts assignment system
  - Bus maintenance history
  - Comprehensive bus overview

- 📊 **Advanced Reporting**
  - Visual analytics and charts
  - Stock level monitoring
  - Usage trends
  - Expenditure tracking
  - Monthly and daily sales reports

- 📋 **Order Management**
  - Order creation and tracking
  - Status updates
  - Order history
  - Filtered view options

## Prerequisites

- Python 3.8+
- MySQL Server
- pip (Python package manager)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/vbs-0/advanced_inventory-management.git
cd advanced_inventory-management
```

2. Create a virtual environment:
```bash
python -m venv venv
```

3. Activate the virtual environment:
- Windows:
```bash
venv\Scripts\activate
```
- Linux/Mac:
```bash
source venv/bin/activate
```

4. Install required packages:
```bash
pip install -r requirements.txt
```

5. Configure MySQL Database:
- Create a new MySQL database named 'inventory_db'
- Update the database URI in app.py:
```python
app.config['SQLALCHEMY_DATABASE_URI'] = 'mysql://username:password@localhost/inventory_db'
```

6. Initialize the database:
```bash
python
>>> from app import app, db
>>> with app.app_context():
...     db.create_all()
```

## Running the Application

1. Start the application:
```bash
python app.py
```

2. Access the application at: `http://localhost:5000`

## User Roles and Permissions

### Admin
- Full system access
- User management
- System configuration
- Access to all reports and features

### Manager
- Category management
- Order approval
- Access to reports
- Product management

### Supervisor
- Product oversight
- Parts assignment
- Basic reporting access

### User
- View products
- Create orders
- Basic access

## Features Guide

### 1. Product Management
- Add/Edit/Delete products
- Set low stock thresholds
- Assign categories
- Track stock levels

### 2. Bus Management
- Add new buses with details
- Track bus information
- Assign parts to buses
- View bus maintenance history

### 3. Order Processing
- Create new orders
- Track order status
- View order history
- Filter and search orders

### 4. Reporting
- View stock levels
- Track expenditure
- Monitor sales trends
- Generate usage reports

### 5. Bulk Upload
- Upload multiple records at once
- Support for buses, products, and categories
- Sample templates available
- Data validation

## API Endpoints

### Authentication
- `/login` - User login
- `/logout` - User logout

### Products
- `/products` - View all products
- `/products/add` - Add new product
- `/products/edit/<id>` - Edit product
- `/products/delete/<id>` - Delete product

### Categories
- `/categories` - View all categories
- `/categories/add` - Add new category
- `/categories/edit/<id>` - Edit category
- `/categories/delete/<id>` - Delete category

### Orders
- `/orders` - View all orders
- `/orders/create` - Create new order
- `/orders/<id>/update-status` - Update order status

### Buses
- `/buses` - View all buses
- `/buses/add` - Add new bus
- `/buses/edit/<id>` - Edit bus
- `/buses/delete/<id>` - Delete bus

### Reports
- `/reports` - View all reports
- `/api/chart-data` - Get chart data

## Bulk Upload Templates

Sample CSV templates are available for:
- Bus data
- Product data
- Category data

Access templates at: `/download-sample/<type>`

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
