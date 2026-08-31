# E-Certificate Management System

This is a web-based E-Certificate Management System that I developed to make the process of creating, managing and verifying certificates easier.

The main idea behind this project is to generate digital certificates with a unique certificate ID and QR code. The QR code can be scanned to verify whether a certificate is valid or not.

## Features

* User registration and login
* Certificate creation and management
* Generate certificates as PDF
* Unique certificate ID for every certificate
* QR code generation for certificates
* Certificate verification using QR code
* Certificate verification using certificate ID
* Email and OTP functionality
* MySQL database for storing certificate and user details
* Separate frontend and backend

## Technologies Used

### Frontend

* React.js
* JavaScript
* HTML
* CSS
* Axios
* React Router

### Backend

* Node.js
* Express.js
* REST APIs
* MySQL
* Nodemailer
* Multer
* QRCode
* Puppeteer
* bcrypt
* Express Session

## Project Structure

```text
e-certificate-management/
│
├── backend/
│   ├── routes/
│   ├── controllers/
│   ├── models/
│   ├── middleware/
│   └── server.js
│
├── frontend/
│   ├── public/
│   └── src/
│       ├── components/
│       ├── pages/
│       └── services/
│
├── docs/
├── render.yaml
└── README.md
```

## How it works

First, the user can register and log in to the application.

After logging in, certificates can be created by entering the required details. Once a certificate is generated, it gets a unique certificate ID along with a QR code.

The QR code can be scanned to open the verification page. The certificate ID is then checked against the database and the certificate details are displayed if it is valid.

The certificates can also be generated/downloaded as PDF files.

## Running the project locally

### 1. Clone the repository

```bash
git clone https://github.com/ChandrikaMudhiraj/e-certificate-management.git
cd e-certificate-management
```

### 2. Backend setup

```bash
cd backend
npm install
```

Create a `.env` file in the backend folder and add the required database and email configuration.

Example:

```env
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_DATABASE=ecerti

EMAIL_USER=your_email
EMAIL_PASS=your_email_password

SESSION_SECRET=your_secret
```

### 3. Database setup

Create a MySQL database and configure the database details in the `.env` file.

```sql
CREATE DATABASE ecerti;
```

Use the database/schema files provided in the project to create the required tables.

### 4. Start the backend

```bash
npm start
```

### 5. Start the frontend

Open another terminal and run:

```bash
cd frontend
npm install
npm start
```

The application should then be available at:

```text
http://localhost:3000
```

## Certificate Verification

Each certificate has a unique certificate ID and QR code.

When the QR code is scanned, it takes the user to the certificate verification page. The system checks the certificate ID with the database and shows the certificate information if it exists.

This makes it easier to verify certificates without having to manually check the original records.

## Deployment

The project can be deployed using services such as Render and Vercel.

The backend requires the necessary environment variables and a MySQL database connection to work correctly after deployment.

## What I learned from this project

While working on this project, I got hands-on experience with React, Node.js, Express, MySQL and REST APIs. I also worked with authentication, PDF generation, QR codes, email functionality and deploying a full-stack application.

## Future Improvements

Some things I would like to add or improve in the future:

* Better certificate templates
* Admin dashboard
* Different user roles
* More customization options for certificates
* Better mobile responsiveness
* Digital signatures for certificates

## Author

**Eega Chandrika**

This project was developed as part of my academic/full-stack development work.
