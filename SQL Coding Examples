/*Select Even Number IDs and remove duplicates*/
select station.city from STATION where mod(station.ID,2)=0 group by station.city;

/*Select the difference between total records and distinct records*/
select (count(Station.city) - Count(distinct Station.city)) from station;

/*Select the two cities with the shortest and longest CITY names, as well as their respective lengths (i.e.: number of characters in the name). If there is more than one smallest or largest city, choose the one that comes first when ordered alphabetically. */
select city,length(city) from station where length(city) in (select max(length(city)) from station union select min(length(city)) from station) order by length(city) desc,city asc limit 2;

/*Select CITY names starting with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates. */
select station.city from station where lower(SUBSTR(station.city,1,1)) in ('a','e','i','o','u');

/*Select CITY names ending with vowels (i.e., a, e, i, o, or u) from STATION. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,length(station.city),1)) in ('a','e','i','o','u');

/* Select CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,length(station.city),1)) in ('a','e','i','o','u') and lower(SUBSTR(station.city,1,1)) in ('a','e','i','o','u');

/* Select CITY names from STATION that do not start with vowels. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,1,1)) not in ('a','e','i','o','u');

/* Select CITY names from STATION that do not end with vowels. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,length(station.city),1)) not in ('a','e','i','o','u');

/* Select CITY names from STATION which do not have vowels (i.e., a, e, i, o, and u) as their first or last characters. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,length(station.city),1)) not in ('a','e','i','o','u') or lower(SUBSTR(station.city,1,1)) not in ('a','e','i','o','u');

/* Select CITY names from STATION which do not have vowels (i.e., a, e, i, o, and u) as their first and do not have vowels as their last characters. Your result cannot contain duplicates. */
select distinct station.city from station where lower(SUBSTR(station.city,length(station.city),1)) not in ('a','e','i','o','u') and lower(SUBSTR(station.city,1,1)) not in ('a','e','i','o','u');

/* Select the Name of any student in STUDENTS who scored higher than  Marks. Order your output by the last three characters of each name. If two or more students both have names ending in the same last three characters (i.e.: Bobby, Robby, etc.), secondary sort them by ascending ID. */
Select students.name from students where students.marks > 75 order by right(students.name,3) asc, students.id asc;

/* Write a query that prints a list of employee names from the Employee table in alphabetical order. */
Select name from employee order by name;

/* Write a query that prints a list of employee names (i.e.: the name attribute) for employees in Employee having a salary greater than per month who have been employees for less than months. Sort your result by ascending employee_id. */
select name from employee where salary > 2000 and months <10 order by employee_id asc;

/* Write a query identifying the type of each record in the TRIANGLES table using its three side lengths. Output one of the following statements for each record in the table*/
SELECT CASE
WHEN A + B <= C OR A + C <= B OR B + C <= A THEN 'Not A Triangle'
WHEN A = B AND B = C THEN 'Equilateral'
WHEN A = B OR B = C OR A = C THEN 'Isosceles'
ELSE 'Scalene'
END
FROM TRIANGLES;

/* Query a count of the number of cities in CITY having a Population larger than 100,000*/
Select count(district) from city where population > 100000;

/* Query the total population of all cities in CITY where District is California. */
Select sum(population) as TotalPop from city where district='California';

/*Query the average population of all cities in CITY where District is California. */
select avg(population) as AvgPop from city where district='California';

/*Query the average population for all cities in CITY, rounded down to the nearest integer. */
Select floor(avg(Population)) as AvgPop from city;

/*Query the sum of the populations for all Japanese cities in CITY. The COUNTRYCODE for Japan is JPN.*/
Select sum(population) as TotalPop from city where countrycode='JPN';

/*Query the difference between the maximum and minimum populations in CITY. */
Select (max(population)-min(population)) as PopDiff from city;
