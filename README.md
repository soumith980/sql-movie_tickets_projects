# Movie Ticket Booking System

## Project Overview

This project is a Movie Ticket Booking System developed using MySQL.

## Database Tables

- Users
- Movies
- Theaters
- Shows
- Bookings

## SQL Concepts Used

- CREATE TABLE
- INSERT
- UPDATE
- DELETE
- JOINs
- Aggregate Functions
- Subqueries
- Views
- Stored Procedures

## Key Queries & Analysis

**###Top 5 most booked movies**
-  select m.movie_name ,count(m.movie_name) as total from bookings b join shows s on b.show_id=s.show_id join movies m on s.movie_id=m.movie_id
 group by m.movie_name order by total desc limit 5;


![image alt](https://github.com/soumith980/sql-movie_tickets_projects/blob/c31f0cfd314eddb5d1b0321b497de3e3c747467c/images/Top%205%20movies.png)


**###Most active users**
-select u.name,count(b.booking_id) as hight_bookings from bookings b join users U on b.user_id =u.user_id group by u.user_id order by hight_bookings desc;










**Monthly booking report**
- select date_format(booking_date,"%Y-%m")as months, count(booking_id) as total_bookings from bookings group by months;







 ** Highest revenue-generating movie**
select m.movie_name, sum(b.total_amount) as total_revenu from bookings b join shows s on b.show_id=s.show_id join movies m on s.movie_id = m.movie_id 
group by m.movie_name order by total_revenu desc limit 1;







 
**- User spending analysis**
select u.user_id,u.name, sum(b.total_amount) as total_amount from bookings b join users u on b.user_id=u.user_id group by u.user_id order by total_amount desc;

