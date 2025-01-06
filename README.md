# PL-SQL-Project

Name of Student:- Sayam Balasaheb Godase
Email of the Student:- sayamgodase@gmail.com

Title Of Project:- Hotel Reservation System

Description of the Project:-
The Hotel Reservation System is a database-driven solution designed to manage room bookings, track availability, and store customer details efficiently. This system aims to streamline the reservation process, prevent booking conflicts, and provide insights into hotel occupancy rates.

Key Features:

Room Bookings:
Maintain detailed records of room reservations, including customer information, booking dates, and room details.
Availability Management:
Dynamically track room availability to ensure real-time updates and accurate status for potential customers.
Technical Components:

PL/SQL Functions:

Functions will be implemented to check the availability of rooms for a given date range.
These functions ensure that customers can only book rooms that are vacant during the requested period.
Triggers for Double-Booking Prevention:

Database triggers will be written to enforce constraints preventing multiple bookings of the same room for overlapping time periods.
Triggers will act as a safeguard to maintain data integrity and eliminate booking conflicts.
Occupancy Rate Reports:

SQL queries will be used to generate comprehensive reports on hotel occupancy rates over specified timeframes.
Reports will help hotel management understand room utilization patterns, peak periods, and areas for optimization.

Devolpment of the Project:-
     The Hotel Reservation System is designed to streamline and manage hotel reservations efficiently. It consists of a robust database structure, PL/SQL functions, triggers, and SQL queries to ensure accurate tracking of bookings, prevention of conflicts, and generation of actionable reports.

 Database Design:
   1) Tables:

      Customers: Stores customer details like name, email, and phone number.
      Rooms: Tracks room details such as room number, type (e.g., Single, Double, Suite), and price per night.
      Bookings: Manages booking information, linking customers and rooms, and includes check-in and check-out dates.
      
   2) Relationships:

      A foreign key in Bookings ensures data integrity by linking CustomerID to Customers and RoomID to Rooms.

   3) Primary Keys:

      Unique identifiers like CustomerID, RoomID, and BookingID are set as primary keys.

PL/SQL Functions:
   1) CheckRoomAvailability:

      A custom function ensures that a room is available for a specified date range.
      It checks for overlapping bookings using SQL conditions and returns either "Available" or "Not Available."
    
      Key Logic:

         The function compares the requested check-in and check-out dates with existing bookings to determine availability, ensuring that no dates overlap.

Triggers for Conflict Prevention:
    1) PreventDoubleBooking:
         A database trigger prevents multiple bookings for the same room within overlapping dates.
         It invokes the CheckRoomAvailability function and raises an error if the room is unavailable.
         Significance:
             This trigger ensures data consistency and avoids operational issues caused by double bookings.

Occupancy Rate Report:
     1) SQL Query:
         An SQL query calculates occupancy rates by determining the percentage of booked rooms for each room type.
         The report includes details like total rooms, booked count, and occupancy rate for better decision-making.
         Management Insights:
              Helps identify high-demand room types, optimize pricing strategies, and allocate resources effectively.

Testing Of the Project:-

Testing the Hotel Reservation System involved validating various aspects of the database and its functionalities to ensure accuracy, reliability, and consistency. The database was tested by inserting, updating, and deleting data in the Customers, Rooms, and Bookings tables to confirm that all relationships and constraints were functioning correctly. The CheckRoomAvailability function was rigorously tested with various date ranges, including overlapping and non-overlapping scenarios, to verify that it accurately identified room availability.

The PreventDoubleBooking trigger was tested by simulating multiple booking attempts for the same room within overlapping date ranges. The trigger successfully raised an error when conflicts were detected, ensuring no double bookings occurred. Occupancy reports were generated and reviewed for different timeframes to validate that the calculations for booked rooms and occupancy rates were accurate. Edge cases, such as check-in and check-out on the same day or bookings spanning multiple months, were also tested to confirm the system's reliability under unusual conditions. Finally, the end-to-end booking process was simulated to ensure that all functionalities, from booking creation to report generation, worked seamlessly.

Conclusion:-
     The Hotel Reservation System is a comprehensive solution that ensures operational efficiency and customer satisfaction. It eliminates booking conflicts, provides real-time room availability updates, and equips hotel management with essential insights for decision-making. With its modular design, the system is scalable and can accommodate additional features as business needs evolve.
