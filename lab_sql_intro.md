-- 1. Review the tables in the database.

use sakila;
Show tables;

-- 2. Explore tables by selecting all columns from each table or using the in built review features for your client.

Select * from sakila.film;
Select * from sakila.actor;

-- 3. Select one column from a table. Get film titles.

select title from sakila.film;

-- 4. Select one column from a table and alias it. Get unique list of film languages under the alias language. Note that we are not asking you to obtain the language per each film, but this is a good time to think about how you might get that information in the future.

select title as movie_title from sakila.film;
select distinct name as unique_languge from sakila.language;

-- 5. Using the select statements and reviewing how many records are returned, can you find out how many stores and staff does the company have? Can you return a list of employee first names only?*/

select count(*) as 'Number of Stores' from sakila.store;
select count(*) as 'Number of Staffs' from sakila.staff_list;

-- Bonus: How many unique days did customers rent movies in this dataset?

select count(distinct(DATE(rental_date))) as Dates from rental;