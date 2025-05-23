# second-hand-car-dealer----SQL



create database cars;

use cars;
-- READ DATA--
SELECT*FROM car_dekho;
-- Total Cars : To get a count of total records--
select count(*) from car_dekho;
-- Manager asked the employeehow many cars available in 2023?--
 select count(*) from car_dekho where year =2023;
 -- manager asked how many cars available 2021,2021,2022, here we are using groupby--
 select count(*) from car_dekho where year in (2020,2021,2022) group by year;
 -- client asked me to print the total of all car by year. I don't see all the detail.--
 select year,count(*) from car_dekho group by year;
 -- client asked to car dealer agent how many diesel car will there be in 2020?--
 select count(*)from car_dekho where year = 2020 and fuel = "Diesel";
 -- how many petrols car avialable in 2020?-- #51
 select count(*) from car_dekho where year = 2020 and fuel = "Petrol";
 -- the manageer told the employee to give a print all the fuel cars (petrol,diesel and cng)come by all year--
 select year, count(*) from car_dekho where fuel = 'petrol' group by year;
 select year, count(*) from car_dekho where fuel = 'diesel' group by year;
 select year, count(*) from car_dekho where fuel = 'cng'    group by year;    
 -- manager said there were more than 100 car in a given year, which year had more than 100 cars? --
 select year, count(*) from car_dekho group by year having count(*)>100;
 select year, count(*) from car_dekho group by year having count(*)<50;
 -- manager said the employee all cars count detail between 2015 to 2023; we need a complete list,--
 select count(*)from car_dekho where year between 2015 and 2023;
 -- manager said to the employee all cars detail between 2015 to 2023 we neeedcomplete list--
 select*from car_dekho where year between 2015 and 2023;
 
 -- END--
 
