# Sales-Reporting-System

1. Setup and Configuration
Prerequisites:
Eclipse IDE: Install Eclipse IDE for Java Developers.
MySQL Server: Install MySQL server and MySQL Workbench.
JDBC Driver: Download the MySQL Connector/J (JDBC driver) and add it to your project in Eclipse.(the zip folder already has it so no need to install it.)

2. Database Schema Creation
create the required tables in the MySQL database using MySQL Workbench.
CREATE DATABASE RetailSalesDB;

USE RetailSalesDB;

CREATE TABLE Product (
    product_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    category VARCHAR(100),
    price DECIMAL(10, 2)
);

CREATE TABLE Customer (
    customer_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100),
    phone VARCHAR(15),
    address VARCHAR(255)
);

CREATE TABLE Sales (
    sale_id INT PRIMARY KEY AUTO_INCREMENT,
    product_id INT,
    customer_id INT,
    sale_date DATE,
    quantity INT,
    total_amount DECIMAL(10, 2),
    FOREIGN KEY (product_id) REFERENCES Product(product_id),
    FOREIGN KEY (customer_id) REFERENCES Customer(customer_id)
);

3.Unzip the 28470857 folder and open it in Eclipse IDE.

4.After setting up the folder, run the application, and ensure that it interacts with the MySQL database as expected.
