# online-stationery-shop
# Online Stationery Shop

A responsive e-commerce web application project for a small stationery shop, built using the MERN stack.

The system will bring customer orders, stock, supplier purchases, deliveries and cash-on-delivery records into one application.

## Project Status

The proposal and initial design work are complete. The project is entering the development stage.

The features below describe the planned system.

## Problem Statement

Small stationery shops often manage orders, stock and supplier requests through separate messages and handwritten records. This can lead to missed orders, incorrect stock figures, delayed deliveries and difficulty tracking collected cash.

This project aims to provide a central system that makes shopping easier for customers and helps the shop manage its daily operations.

## Objectives

- Provide a searchable stationery catalogue with prices and availability.
- Allow customers to place cash-on-delivery orders.
- Maintain accurate stock and order records.
- Coordinate supplier purchases and goods receipts.
- Support order preparation and delivery management.
- Track collected cash and verify handovers to the shop owner.

## User Roles

| Role | Main Responsibilities |
|------|-----------------------|
| Customer | Browse products, manage the cart, place orders and view order progress. |
| Shop Staff | Confirm orders, prepare packages, dispatch orders and receive supplier goods. |
| Shop Owner | Manage products, accounts, purchases, delivery assignments and cash reconciliation. |
| Supplier | Respond to assigned purchase orders and record approved shipments. |
| Delivery Person | View assigned deliveries, record delivery outcomes and submit collected cash. |

Public registration will create Customer accounts only. The shop owner will create staff, supplier and delivery accounts.

## Planned Features

### Customer
- Registration and login
- Product browsing, search and category filtering
- Product details and availability
- Shopping cart
- Cash-on-delivery checkout
- Order history and status updates
- Cancellation of eligible Pending orders

### Shop Staff
- Order review and confirmation
- Packing checks and dispatch
- Supplier goods receipt
- Recording accepted, missing and damaged quantities

### Shop Owner
- Product and category management
- Staff and partner account management
- Purchase order creation
- Supplier revision approval
- Delivery assignment
- COD cash reconciliation

### Supplier
- Assigned purchase order access
- Acceptance, rejection or proposed quantity changes
- Shipment recording after approval

### Delivery Person
- Assigned delivery details
- Successful and unsuccessful delivery updates
- COD collection records
- Cash handover submission

## Technology Stack

| Area | Technology |
|------|------------|
| Frontend | React.js with Vite |
| Styling | CSS and Bootstrap |
| Backend | Node.js and Express.js |
| Database | MongoDB |
| Database Modelling | Mongoose |
| API Communication | Fetch API |
| Version Control | Git and GitHub |
| API Testing | Postman |
| Diagrams and Wireframes | draw.io |



## Getting Started

### Prerequisites

- A Node.js LTS version compatible with the project dependencies
- npm
- A MongoDB database
- Git or GitHub Desktop
- Visual Studio Code or another code editor

### Clone the Repository

In GitHub Desktop:

1. Select **File → Clone Repository**.
2. Select this repository.
3. Choose a local folder and click **Clone**.
4. Open the cloned project in Visual Studio Code.

Create the frontend and backend directly inside the repository root.

### Local Development

After the initial scaffolding and development scripts have been created, install dependencies in each application:

```bash
cd frontend
npm install
```

```bash
cd backend
npm install
```

Create local `.env` files using the corresponding `.env.example` files.

Start each application in a separate terminal using the scripts defined in its `package.json`. Exact startup commands and local URLs will be documented after the initial setup is verified.

## Environment Configuration

The planned environment variables are:

| Application | Variable | Purpose |
|-------------|----------|---------|
| Frontend | `VITE_API_BASE_URL` | Backend API base URL |
| Backend | `PORT` | Backend server port |
| Backend | `MONGODB_URI` | MongoDB connection string |

Authentication-related variables will be documented when authentication is implemented.

Keep database credentials and other secrets in backend environment variables. Do not commit `.env` files or place secrets in frontend code.

## Main Business Rules

- Stock and prices are checked again during checkout.
- Order creation and stock deduction must succeed together.
- Repeated checkout submissions must not create duplicate orders.
- Customers can cancel only Pending orders.
- Eligible cancellations restore stock once.
- Packing and dispatch do not deduct stock again.
- Supplier quantity revisions require owner approval before shipment.
- Stock increases only when accepted goods are received.
- Delivery personnel can update only their assigned deliveries.
- COD collection and owner cash verification are separate actions.
- Permissions and record ownership are checked by the backend.

## Testing Plan

Testing will cover:

- Registration, login and access permissions
- Product search and management
- Cart quantities and total calculations
- Checkout validation and duplicate submissions
- Stock updates and simultaneous purchases
- Order cancellation and status changes
- Supplier approval and goods receipt
- Delivery outcomes and cash reconciliation
- Responsive layouts

Actual results and identified defects will be recorded during development.
hor

**Jayani Shehara**
