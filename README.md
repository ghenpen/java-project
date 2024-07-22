# Library Management System
# Overview
This Library Management System is designed to manage the core functionalities of a library. It supports the management of authors, books, loans, members, publishers, reservations, and reviews. The system allows users to perform various actions such as finding, listing, creating, updating, and deleting records for these entities.

# Project Structure
The project is organized into several packages and classes, each responsible for a specific aspect of the library management system:

Model: Contains the data models for the entities in the system (e.g., Authors, BookCopies, Loans, Members, Publishers, Reservations, Reviews).
Services: Contains the service classes that handle the business logic for each entity (e.g., AuthorService, BookCopiesService, LoanService, MembersService, PublisherService, ReservationService, ReviewsService).
Database: Contains the DatabaseManager class, which handles database connections and operations.
Reader: Contains the Reader class, which is responsible for interacting with the user via the console and invoking the appropriate service methods based on user input.
DateUtils: Utility class for handling date operations.
Exceptions: Contains custom exceptions used in the project.
Reader Class
The Reader class is the main entry point for the application. It provides a command-line interface for users to interact with the system. The class initializes the services and database manager, and it uses a Scanner to read user input. Based on the user commands, it performs various actions related to authors, books, loans, members, publishers, reservations, and reviews.

# Main Functionalities
Custom Actions:

findAuthorsWithMostBooks: Finds authors with the most books in the library.
listAuthorsByLastName: Lists all authors sorted by their last names.
listBookCopiesByCondition: Lists all book copies by their condition.
findBooksWithMostCopies: Finds books with the most copies available in the library.
listLoansByMember: Lists all loans by a specific member.
findMostLoanedBooks: Finds the most loaned books in the library.
checkResourceAvailability: Checks the availability of a specific resource.
showExpiredReservations: Shows all expired reservations.
CRUD Actions:

findById: Finds an entity by its ID (supports Author, BookCopies, Loan, Members, Publisher, Reservation, Reviews).
findAll: Lists all entities of a specific type (supports Author, BookCopies, Loan, Members, Publisher, Reservation, Reviews).
create: Creates a new entity (supports Author, BookCopies, Loan, Members, Publisher, Reservation, Reviews).
update: Updates an existing entity (supports Author, BookCopies, Loan, Members, Publisher, Reservation, Reviews).
delete: Deletes an entity by its ID (supports Author, BookCopies, Loan, Members, Publisher, Reservation, Reviews).
# Command-Line Interface
The startReader method in the Reader class starts an infinite loop, prompting the user to enter an action name. The action is then processed by a switch statement, which calls the appropriate method to handle the action.

