# shopflow-website
ShopFlow Store – Full Stack Cloud Database Project

This project is my deployed e-commerce demo for the AI ShopFlow E-Commerce Database Analytics Project. It uses a MySQL database hosted on Aiven, Netlify serverless functions as the backend API, and a simple HTML/JavaScript frontend. The goal was to build a real end-to-end system that loads and displays data from the cloud securely.

Live Website
https://polite-sprite-9a4e63.netlify.app/
The site connects to a live cloud database on Aiven and displays product data, customer search results, and analytics.
The dataset itself is sample/mock data provided for the course and imported from CSV files(not included).

Final Project Notebook:
Google Colab Notebook (Full Data Cleaning + Import Pipeline):
CISS340_E-commerce_final_Bradburn.ipynb

Repository includes:
CISS340_E-commerce_final_Bradburn.ipynb – full project notebook
https://github.com/amandabradburn-ciss/shopflow-website/blob/main/CISS340_E-commerce_final_Bradburn.ipynb
/netlify/functions/ – backend API (products, search, customer, analytics)
Frontend files – HTML, CSS, JavaScripts

Project Setup Instructions
1. Clone the repository
   git clone https://github.com/YOUR-USERNAME/ShopFlow.git
   cd ShopFlow
2. Install Netlify CLI (for local development)
   npm install -g netlify-cli
3. Add your environment variables
   Create a .env file or configure them in Netlify:
   DB_HOST=
   DB_PORT=
   DB_USER=
   DB_PASSWORD=
   DB_DATABASE=
   DB_SSL=true
   Aiven requires SSL, so the functions must connect with encryption enabled.
4. Run the site locally
   netlify dev
This launches the frontend and the serverless API functions in one environment.

How the system works:
Google Colab loads and cleans CSV data, then imports it into Aiven MySQL.
Netlify serverless functions (products, search, customer, analytics) query the database securely.
The frontend reads the API responses and displays products, customer info, and analytics.
All SQL queries use parameterized statements to prevent injection.
The deployed site connects to Aiven live—no mock data.

Tech Used:
MySQL on Aiven (SSL required)
Netlify serverless functions (Node.js)
HTML / CSS / JavaScript frontend
Google Colab (data loading + SQLAlchemy)
