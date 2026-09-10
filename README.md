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


**###Most active users**
- Monthly booking report
- Highest revenue-generating movie
- User spending analysis
