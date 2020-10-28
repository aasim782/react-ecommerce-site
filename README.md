# TheStore eCommerce Platform

Live Demo - https://react-ecommerce-site.herokuapp.com/

### Features

- Shopping cart
- Product reviews & ratings
- Top rated products carousel
- Product pagination
- Product search
- User profile maintenance and order list
- Admin product management
- Admin user management
- Admin Order details page
- Mark orders as delivered
- Checkout process (shipping address, payment method, etc)
- PayPal / credit card integration
- Database seeder (products & users)

## Usage

ES Modules in Node
Uses ECMAScript Modules in the backend in this project. Be sure to have at least Node v14.6+ or you will need to add the "--experimental-modules" flag.

Also, when importing a file (not a package) to the backend section, be sure to add .js at the end or you will get a "module not found" error

Since this project uses MongoDB as the database and paypal sandbox as a test payment authenticator, you should have accounts set up with these tools in order to have the uri and ids/keys needed to use these products.

### Env Variables

Create an .env file in then root and add the following

```bash
NODE_ENV = development
PORT = 5000
MONGO_URI = your mongodb uri
JWT_SECRET = 'abc123'
PAYPAL_CLIENT_ID = your paypal client id
```

### Install Dependencies (frontend & backend)

```bash
npm install
cd frontend
npm install
```

# Run

## Run frontend (:3000) & backend (:5000)

```bash
npm run dev
```

## Run backend only

```bash
npm run server
```

Build & Deploy

## Create frontend prod build

```bash
cd frontend
npm run build
```

There is a Heroku postbuild script, so if you push to Heroku, no need to build manually for deployment to Heroku

Seed Database
You can use the following commands to seed the MongoDB database with some sample users and products as well as destroy all data. (Note that the import script, destroys all users and products before importing them)

## Import data

```bash
npm run data:import
```

## Destroy data

```bash
npm run data:destroy
```

#### MIT License
