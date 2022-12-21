# SQL-week-Home-work-1

Which destination in the flights database is the furthest distance away, based on information in the flights table. Show the SQL query(s) that support your conclusion.  

 SELECT DISTINCT flight, origin, dest, distance AS 'furthest distance' FROM flights WHERE distance IN (select max(distance) from flights); Try it Yourself
 

2 What are the different numbers of engines in the planes table? For each number of engines, which aircraft have the most number of seats? Show the SQL statement(s) that support your result.   SELECT engines, MAX(seats) FROM planes GROUP BY engines; Try it Yourself
 

3 Show the total number of flights.   SELECT COUNT(*) FROM flights; Try it Yourself
 

4 Show the total number of flights by airline (carrier).   SELECT carrier, COUNT(*) FROM flights GROUP BY carrier; Try it Yourself
 

5 Show all of the airlines, ordered by number of flights in descending order.   SELECT carrier, COUNT(*) AS FlightCount FROM flights GROUP BY carrier ORDER BY FlightCount DESC; Try it Yourself
 

6 Show only the top 5 airlines, by number of flights, ordered by number of flights in descending order.   SELECT carrier, COUNT(*) AS FlightCount FROM flights GROUP BY carrier ORDER BY FlightCount DESC LIMIT 5; Try it Yourself
 

7 Show only the top 5 airlines, by number of flights of distance 1,000 miles or greater, ordered by number of flights in descending order.   SELECT carrier, COUNT(*) AS FlightCount FROM flights WHERE distance >=1000 GROUP BY carrier ORDER BY FlightCount DESC LIMIT 5; Try it Yourself
 

8 Create a question that (a) uses data from the flights database, and (b) requires aggregation to answer it, and write down both the question, and the query that answers the question. 
Question: 
Create a query that show top 5 airlines, by number of flights in the month of October, ordered by flights number from heights.   SELECT carrier, COUNT(*) as FlightCount FROM flights WHERE MONTH = 10 GROUP BY carrier ORDER BY FlightCount DESC LIMIT 5; Try it Yourself
 

ADMISSIONS | ABOUT
Please email to: kleber.perez@live.com for any suggestion. 
SQL Bridge Week 1 Assignment - MSDS 2019 Program.

