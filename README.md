# QA Dummy E-Commerce API

A ready-to-run REST API for teaching and practicing API testing with Postman.

## Tech Stack

- Node.js
- Express
- JSON files as a simple database
- Postman for API testing

## 1. Prerequisites

Install Node.js (LTS).

Check:

```bash
node -v
npm -v
```

## 2. Install

Open a terminal inside this project:

```bash
npm install
```

## 3. Start the API

```bash
npm start
```

You should see:

```text
QA Dummy API running at http://localhost:3000
```

Open:

```text
http://localhost:3000
```

## Login credentials

```text
Email: nandish@test.com
Password: Test@123
```

Demo token:

```text
qa-demo-token-12345
```

## Main endpoints

### Authentication

```text
POST /api/login
```

### Users

```text
GET    /api/users
GET    /api/users/:id
POST   /api/users
PUT    /api/users/:id
PATCH  /api/users/:id
DELETE /api/users/:id
```

### Products

```text
GET    /api/products
GET    /api/products/:id
POST   /api/products
PUT    /api/products/:id
DELETE /api/products/:id
```

### Orders

```text
POST   /api/orders
GET    /api/orders
GET    /api/orders/:id
DELETE /api/orders/:id
```

## Authorization

All Users, Products and Orders APIs require:

```text
Authorization: Bearer qa-demo-token-12345
```

In Postman, import the included collection. It contains a `baseUrl` variable and a `token` variable.

## Suggested teaching flow

1. GET users
2. Login
3. Capture token
4. GET users with token
5. Create user
6. Get user
7. Update user
8. Delete user
9. GET products
10. Create product
11. Create order
12. Validate order
13. Negative testing
14. Add Postman assertions
15. API chaining
16. Collection Runner

## Useful negative scenarios

- Login with wrong password
- Login without email
- Call protected API without token
- Invalid user ID
- Duplicate email
- Missing mandatory field
- Negative product price
- Negative product stock
- Invalid product ID
- Order with quantity 0
- Order with insufficient stock
- Invalid endpoint

## Resetting test data

The API modifies the JSON files during POST/PUT/PATCH/DELETE operations.

To reset the original data, restore:

- `data/users.json`
- `data/products.json`
- `data/orders.json`

The included Postman collection is designed for training and is not intended as a production authentication system.
