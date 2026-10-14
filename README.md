# Billing Receipt Management

This repository contains a React frontend and a Spring Boot backend.

## Project structure

- `client/` - React application built with Vite
- `billingsoftware/` - Spring Boot REST API
- `billing_app.sql` - MySQL table definitions

## Backend configuration

The backend uses environment variables for credentials. Configure these before starting it:

| Variable | Purpose |
| --- | --- |
| `DB_URL` | MySQL JDBC URL (defaults to `jdbc:mysql://localhost:3306/billing_app`) |
| `DB_USERNAME` | MySQL username (defaults to `root`) |
| `DB_PASSWORD` | MySQL password (defaults to empty) |
| `JWT_SECRET` | Secret used to sign JWTs; set a long, random value |
| `AWS_ACCESS_KEY` | Optional AWS access key |
| `AWS_SECRET_KEY` | Optional AWS secret key |
| `AWS_REGION` | AWS region (defaults to `ap-south-1`) |
| `AWS_BUCKET_NAME` | Optional S3 bucket name |
| `RAZORPAY_KEY_ID` | Optional Razorpay key ID |
| `RAZORPAY_KEY_SECRET` | Optional Razorpay key secret |

Create the MySQL database, apply `billing_app.sql`, and set the backend variables in your shell before running the Spring Boot application.

## Frontend

Install dependencies and start the Vite development server from `client/`:

```sh
npm install
npm run dev
```

Uploaded files, local environment files, and generated build output are excluded from Git.
