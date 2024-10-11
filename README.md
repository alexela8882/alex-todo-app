# From original Repositories

- [Frontend Repository](https://github.com/alexela8882/todo-vue3-lara11.git)
- [Backend Repository](https://github.com/alexela8882/todo-vue3-lara11-be.git)

# Project Setup Instructions

This document outlines the steps to set up and run both the backend (Laravel) and frontend parts of the project.

## Prerequisites

Before starting, ensure that the following are correctly installed and configured:

- PHP >= 7.3 (or as required by Laravel)
- Composer
- Node.js and npm
- MySQL or another supported database
- A properly configured `.env` file for the backend, including database credentials

## Backend Installation (Laravel)

### Step 1: Install Dependencies

Navigate to the backend folder and run the following command to install all necessary dependencies:

```bash
composer install
```

### Step 2: Configure Environment Variables

Ensure the `.env` file is properly configured, especially the database connection settings. You may copy the example file if it doesn't already exist:

```bash
cp .env.example .env
```

After copying, set the correct values for the database and other necessary configurations.

### Step 3: Generate Application Key

Generate the application key using the command:

```bash
php artisan key:generate
```

### Step 4: Run Migrations

Run the following command to apply all migrations:

```bash
php artisan migrate
```

### Step 5: Seed the Database

To populate the database with initial data, run:

```bash
php artisan db:seed
```

### Step 6: Start the Backend Server

By default, the backend server is configured to run on `localhost:8000`. To start the server, run:

```bash
php artisan serve --host=localhost --port=8000
```

If the port `8000` is in use, adjust the port in the frontend or backend to avoid conflicts.

---

## Frontend Installation

### Step 1: Install Dependencies

Navigate to the frontend folder and run the following command to install all necessary dependencies:

```bash
npm install
```

### Step 2: Running in Development Mode

If you're running the frontend in development mode, use the following command:

```bash
npm run dev
```

This will start a development server and automatically update the page as you make changes.

### Step 3: Running in Production Mode

If you’re ready to run the frontend in production, use the following command:

```bash
npm run preview
```

---

## Notes

- Ensure both the backend and frontend servers are running on compatible ports to facilitate communication between the two.
- Adjust your configurations accordingly if you're using different environments or setups.
