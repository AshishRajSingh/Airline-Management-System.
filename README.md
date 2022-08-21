# Airline-Management-System.

Airline Management System. AIRLINE MANAGEMENT SYSTEM JAVA Core Project

This project on Airline Management System is the automation of registration process of airline system. The system is able to provide much information like passenger’s information, criminal’s, list of all passengers etc. The system also allows us to add records when a passenger reserves a ticket. For data storage and retrieval we use MySQL Database. It enables us to add any number of records in our database.

Language Used - Java Core Concept Used - Swing IDE Used - NetBeans Database Used - MySQL https://drive.google.com/file/d/1flYQG5eCAn1aIi49xep78kquQw0Et14x/view?usp=sharing

Database 1 - Create table with name cancellation

create table cancellation(pnr_no varchar(10), cancellation_no varchar(10), cancellation_date DATE, fli_code varchar(15));

2 - create table with name flight

create table flight(f_code varchar(10), f_name varchar(20), src varchar(30), dst varchar(30));

3 - create table with name login

create table login(username varchar(20), password varchar(20));

4 - create table with name passenger

create table passenger(pnr_no varchar(10), address varchar(30), nationality varchar(15), name varchar(20), gender varchar(10), ph_no varchar(15), passport_no varchar(20), fl_code varchar(10));

5 - create table with name payment

create table payment(pnr_no varchar(10), ph_no varchar(15), cheque_no varchar(15), card_no varchar(20), paid_amt varchar(10), pay_date DATE);

6 - create table with name reservation

create table reservation(pnr_no varchar(10), ticket_id varchar(10), f_code varchar(10), jny_date DATE, jny_time varchar(10), src varchar(20), dst varchar(20));

7 - create table with name sector

create table sector(flight_code varchar(20), capacity varchar(10), class_code varchar(5), class_name varchar(20));

Airline Management System

Introduction The project “Airline Management System” comprises of a large number of flights which belong to a particular airline. The system we have implemented manages different objects viz. • Airline • Airline Employees • Customers/Traveller Each of these accesses a database schema which has corresponding tables.Web services are used for middleware technology.

Individual Contributions Name Contribution Name ● DB tables creation and modification – FlightDetails, Person ● searching flights, update flights, display flight information, list all flights ● Code Integration Name ● DB tables creation and modification – Traveller, Person, Reservation, Reservation details ● Reservation module – manage reservations, traveller, validations ● Object caching implementation ● Code Integration Name ● DB tables creation and modification – Person, Employee ● Employee module: Create Employee, Delete employee, Update employee info, List/Display employee info, Search employees ● Project report preparation ● Test Harness ● Code Integration Name ● DB tables creation and modification – Person, Payment ● DatabaseConnection Pooling – code implementation ● JMS Implementation ● Test Harness – Soap UI ● Code Integration Name ● DB tables creation and modification ● Profiling module – login, create user, update user, delete user, list customers ● Code Integration

Project Requirements Tier 1 – Client Requirements • Airline management system client has all the functionalities listed as a part of requirements. • A simple UI is used and appropriate error messages are displayed to the users wherever necessary. Some of us in the team have used a front end framework called Bootstrap which contains customizable style sheets and is a faster way to do client side coding.

Tier 2 - Middleware • We have clearly defined interfaces implementing all the required functionalities. • JDBC connection is established for select/insert/update data to database. • JMS is used for publishing the status of flights to all the users who are online.

Tier 3 – Database schema and database creation • My SQL is used for designing our database. The following tables are created in the database, Person, Employee, Traveller, Reservations, Reservation_Details, FlightDetails, Payment

Functional Requirements Implemented • Create a new employee • Delete an existing employee • Create a new Customer • Delete an existing Customer • Create a new reservation • Cancel an existing reservation • Issue a flight ticket • Payment options • List all customers known by the system • List all employees known by the system • List all reservation known by the system • List all flights known by the system • Change a employee/ customer information (name, address, etc) ability to change ALL attributes • Change a flights information (time, source, destination etc) change ALL attributes • Search for a employee based on attributes. • Search for a flight based on attributes • Display information about a employee • Display information about a traveler • Display information about a flight

Non Functional Requirements -Scalability, Performance and Reliability • Object caching is implemented for searching for flights(detailed explanation below) • Database connection pooling is handled(detailed explanation below) • The Person and Employee tables have 5000 records and we are successfully able to handle and show the data for such large number of records in our application. • PreparedStatement is made use of in all the server methods to improve performance. • SQL queries used to access the database are tuned. Some of the things we have focussed on include: Not using Like predicate in queries, using ‘=’ instead of IN when only one record has to be retrieved, using specific column names in select instead of *. • We have tested the flow of all the modules so that nothing crashes thus ensuring reliability

Testing Test Harness We have used Soap UI to test the performance of web services.When a new project is created, we give our wsdl and then add test steps for a specific method. We run the test against certain number of count.
