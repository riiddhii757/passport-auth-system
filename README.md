# Passport Authentication System

This project demonstrates how to implement a **passport-based authentication system** using **Node.js**, **Express**, and **PostgreSQL** with **Google OAuth 2.0**.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/riiddhii757/passport-auth-system.git

2.Navigate to the project folder:
 cd passport-auth-system

3. Install dependencies:
 npm install

4.Create a .env file in the root directory of the project with the following environment variables:
 SESSION_SECRET=your-secret
 PG_USER=your-database-user
 PG_PASSWORD=your-database-password
 PG_HOST=your-database-host
 PG_PORT=5432
 PG_DATABASE=your-database-name
 GOOGLE_CLIENT_ID=your-google-client-id
 GOOGLE_CLIENT_SECRET=your-google-client-secret

Setting Up Google OAuth 2.0
To use Google OAuth 2.0 authentication, you need to create a project on Google Cloud and generate OAuth 2.0 credentials (Client ID and Client Secret).

Steps to Get Your Google OAuth 2.0 Client ID and Client Secret:
Go to the Google Cloud Console.

Create a new project:

Click on the project dropdown in the top-left corner.
Click on "New Project" and fill in the required details (like project name).
Click "Create".
Enable the Google+ API (for authentication):

In the left sidebar, go to APIs & Services → Library.
Search for Google+ API.
Click on Google+ API and click Enable.
Create OAuth 2.0 Credentials:

Go to APIs & Services → Credentials.
Click Create Credentials → OAuth 2.0 Client IDs.
Choose Web Application.
Under Authorized JavaScript Origins, add http://localhost:3000 (if running locally).
Under Authorized Redirect URIs, add http://localhost:3000/auth/google/secrets (for the callback after successful login).
Click Create.
Get the Client ID and Client Secret:

After creating the credentials, you will see the Client ID and Client Secret on the page.
Copy and paste the Client ID and Client Secret into your .env file.
Update .env:

Add the following to your .env file:

GOOGLE_CLIENT_ID=your-client-id-here
GOOGLE_CLIENT_SECRET=your-client-secret-here
Running the Application
Make sure you have your PostgreSQL database set up with the correct user and password.

Start the application:
npm start
Open your browser and navigate to:

http://localhost:3000 to view the home page.
http://localhost:3000/login to log in using local authentication.
http://localhost:3000/auth/google to log in using Google OAuth.
Technologies Used
Node.js
Express.js
Passport.js
PostgreSQL
Google OAuth 2.0
