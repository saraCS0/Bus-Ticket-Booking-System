# Bus Ticketing System

## Overview
The *Bus Ticketing System* is designed to streamline the process of booking bus tickets online. Users can register, log in, and book tickets for various destinations, while administrators can manage stations, trains, and schedules. The system is built using *Java, **JSP, and **SQLite* for data storage.

## Project Demo
Check out the project demo on [YouTube](https://youtu.be/3uQ0uITLEGg).

## Developed By
*Md Rukon Shekh*

## Technologies Used
- *Languages:* Java, JSP, HTML, CSS, JavaScript, AJAX, jQuery, MySQL
- *IDE:* Eclipse JEE
- *Server:* Apache Tomcat
- *Database:* MySQL

I have developed this bus ticket reservation project in my 10th semester. This ticket reservation system project source code is suitable for BE, BTech, MCA, BCA, engineering, BS CS, IT, and software engineering final year students to submit their source code in college or university. I have uploaded the full project source code with the database on GitHub, and you can download this bus booking system for free.

## Core Components

### 1. *User Module*
This module handles user registration, login, and logout functionality. Users can create an account, log in to their dashboard, and manage bookings.

- *Key Classes:*
  - User: Manages user details, including login credentials and booking information.
  - SignUpAction: Oversees the signup process, ensuring data validation and storing user information in the database.
  - Logout: Manages user logout sessions.

- *Code Snippet:*
  java
  public class User {
      private String username;
      private String password;

      public User(String username, String password) {
          this.username = username;
          this.password = password;
      }

      public boolean login() {
          // Logic to authenticate user
      }

      public void logout() {
          // Logic to log out the user
      }
  }
  

### 2. *Booking Module*
The Booking module allows users to search for available trains, choose destinations, and make ticket reservations.

- *Key Classes:*
  - Booking: Manages the booking process, including selecting trains, dates, and destinations.
  - Destination: Manages available destinations for booking.
  - Stations: Handles data related to various train stations.

- *Code Snippet:*
  java
  public class Booking {
      private Train selectedTrain;
      private Destination destination;
      private String date;

      public Booking(Train train, Destination destination, String date) {
          this.selectedTrain = train;
          this.destination = destination;
          this.date = date;
      }

      public void confirmBooking() {
          // Logic to confirm booking
      }
  }
  

### 3. *Train Module*
The Train module deals with all aspects related to train details, such as schedules, seat availability, and departure times.

- *Key Classes:*
  - Train: Stores train details, including train number, schedule, and available seats.
  - TrainManager: Handles the logic for retrieving and displaying train information.

- *Code Snippet:*
  java
  public class Train {
      private String trainNumber;
      private String schedule;
      private int availableSeats;

      public Train(String trainNumber, String schedule, int availableSeats) {
          this.trainNumber = trainNumber;
          this.schedule = schedule;
          this.availableSeats = availableSeats;
      }

      public boolean isAvailable() {
          return availableSeats > 0;
      }
  }
  

### 4. *Database Module*
This module is responsible for connecting the system to the SQLite database. It handles data storage and retrieval for users, bookings, and train schedules.

- *Key Classes:*
  - Database: Contains methods for connecting and interacting with the SQLite database.
  - Helper: Provides utility functions to support database operations, such as queries and connection handling.

- *Code Snippet:*
  java
  public class Database {
      private Connection connection;

      public Database() {
          // Logic to establish a database connection
      }

      public ResultSet executeQuery(String query) {
          // Logic to execute SQL query
      }
  }
  

### 5. *Helper Module*
The Helper module contains utility functions that assist with operations throughout the system, such as formatting, date handling, and database queries.

- *Key Classes:*
  - Helper: Provides commonly used utility functions in the system.

- *Code Snippet:*
  java
  public class Helper {
      public static String formatDate(String date) {
          // Logic to format a date
      }
  }
  

### 6. *Functions Module*
This module manages the core functionalities of the system, including handling train schedules, managing stations, and booking operations.

- *Key Classes:*
  - Functions: Contains business logic for core operations, such as managing stations and train schedules.

- *Code Snippet:*
  java
  public class Functions {
      public static List<Train> getTrainSchedules() {
          // Logic to retrieve train schedules
      }
  }
  

## How to Run the Project

1. *Clone the repository:*
   - Use your preferred Git client or Git command line to clone the repository to your local machine.

2. *Set up the database:*
   - Ensure that the MySQL database is set up with the appropriate tables for users, trains, bookings, and destinations. SQL scripts are provided in the /db folder.

3. *Import the project into Eclipse:*
   - Open Eclipse and go to *File* > *Import*.
   - Choose *Existing Projects into Workspace* and click *Next*.
   - Browse to the directory where you cloned the repository and select it.
   - Click *Finish* to import the project.

4. *Configure the project:*
   - Right-click on the project in the *Package Explorer* and select *Properties*.
   - Make sure that the project is using *Java JDK 1.8* or later.
   - Verify that the database connection is properly configured in the relevant configuration files.

5. *Run the project:*
   - Right-click on the project and select *Run As* > *Run on Server*.
   - Choose the appropriate server (like Apache Tomcat) if prompted, and click *Finish*.
   - The system's functionality can then be accessed through your web browser.

## Features
- *User Registration & Login:* Secure user authentication system.
- *Train Search & Booking:* Users can search for trains and book tickets for various destinations.
- *Station Management:* Admin users can manage stations and schedules.
- *Train Schedules:* Dynamic train schedules with available seat tracking.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Tags
### Final year projects for computer science
### Mini projects for computer science students
### Final year project ideas computer science

