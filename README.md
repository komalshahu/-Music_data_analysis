# -Music_data_analysis
This project involves performing in-depth analysis of a music store database using SQL. By writing optimized queries, we extract insights about customer behavior, music trends, and business performance — all directly from relational database tables.

# SQL PROJECT- MUSIC STORE DATA ANALYSIS
## Question Set 1 - Easy
1. Who is the senior most employee based on job title?
2. Which countries have the most Invoices?
3. What are top 3 values of total invoice?
4. Which city has the best customers? We would like to throw a promotional Music
   Festival in the city we made the most money. Write a query that returns one city that
   has the highest sum of invoice totals. Return both the city name & sum of all invoice
   totals
6. Who is the best customer? The customer who has spent the most money will be
   declared the best customer. Write a query that returns the person who has spent the
   most money

## Question Set 2 — Moderate
1. Write query to return the email, first name, last name, & Genre of all Rock Music
   listeners. Return your list ordered alphabetically by email starting with A
2. Let's invite the artists who have written the most rock music in our dataset. Write a
   query that returns the Artist name and total track count of the top 10 rock bands
3. Return all the track names that have a song length longer than the average song length.
   Return the Name and Milliseconds for each track. Order by the song length with the
   longest songs listed first

## Question Set 3 — Advance
1. Find how much amount spent by each customer on artists? Write a query to return
   customer name, artist name and total spent
2. We want to find out the most popular music Genre for each country. We determine the
   most popular genre as the genre with the highest amount of purchases. Write a query
   that returns each country along with the top Genre. For countries where the maximum
   number of purchases is shared return all Genres
3. Write a query that determines the customer that has spent the most on music for each
   country. Write a query that returns the country along with the top customer and how
   much they spent. For countries where the top amount spent is shared, provide all
   customers who spent this amount

## Database & Tool
--MYSQL

# Import .sql Format Data into MySQL

🚀 Steps to Import the .sql File
## 🔹 Method 1: MySQL Workbench (GUI)
Open MySQL Workbench
Connect to your MySQL server
Create a new schema or use an existing one
Go to File → Open SQL Script and select your .sql file
Click the Execute (⚡ lightning bolt) button
The script will run, creating tables and inserting data

## 🔹 Method 2: MySQL Command Line
Open Command Prompt or Terminal
Run the following command:

mysql -u root -p
Once logged in, create the database:

CREATE DATABASE music_store;
USE music_store;

Exit and run this command to import the .sql file:

mysql -u root -p music_store < "C:\path\to\music_store.sql"

# 🔹 Load .csv File into MySQL
## Option 1: Using LOAD DATA INFILE (faster, needs config)
Enable file import by checking:

SHOW VARIABLES LIKE 'secure_file_priv';

Place the .csv file in the allowed directory
First we need a table with schema for data storing 

create table customer(
   name varchar(255)
   ...............
   ..............
   )
   
Run this command (modify as needed):

LOAD DATA INFILE 'C:/ProgramData/MySQL/MySQL Server 8.0/Uploads/customers.csv'

INTO TABLE customers

FIELDS TERMINATED BY ','

ENCLOSED BY '"'

LINES TERMINATED BY '\n'

IGNORE 1 ROWS;

## Option 2: Using MySQL Workbench GUI

Right-click the table → Table Data Import Wizard

Browse and select the .csv file

Map columns and import
