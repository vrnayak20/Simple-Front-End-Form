# Juice Shop Login Form with Client & Server Validation

## Overview
This repository contains a full-stack login demonstration mimicking the OWASP Juice Shop authentication page. It showcases the difference between front-end user experience validations and authoritative back-end security validations.

The application enforces validation at two distinct tiers:
1. **Client-Side Validation (public/index.html):** JavaScript prevents empty inputs, checks for the `@` character in the email, and verifies a minimum password length of 8 characters before dispatching a network request.
2. **Server-Side Validation (server.js):** An Express.js backend independently receives the payload via a POST request to `/api/login` and re-evaluates all constraints, demonstrating defense-in-depth against direct API attacks or bypassed browser scripts.

## Directory Structure
* `package.json`
* `server.js`
* `public/index.html`

## How to Run the Project

### Prerequisites
* Node.js installed on your machine.

### Setup & Execution
1. Clone the repository: 
   `git clone https://github.com/vrnayak20/Simple-Front-End-Form.git`
2. Navigate into the directory: 
   `cd Simple-Front-End-Form`
3. Install the necessary dependencies: 
   `npm install`
4. Start the application: 
   `npm start`
5. Open your browser and navigate to: 
   `http://localhost:3000`

## Testing Validation
* **Client-side:** Attempt submitting blank fields or a short password to trigger inline DOM error notices.
* **Server-side:** Submit valid inputs (e.g., `user@example.com` and `password123`) to receive a verified `200 OK` response directly from the Node.js backend.
