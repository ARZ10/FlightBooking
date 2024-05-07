# Flight Booking System

## Overview
The Flight Booking System is a Java-based application that simulates the process of booking flights. This system comprises several classes that represent flights, passengers, tickets, and a manager class to handle operations related to flight bookings.

## Class Descriptions

### 1. Flight
**Attributes**:
- `flightNumber (int)`: Unique identifier for the flight.
- `origin (String)`: Starting point of the flight.
- `destination (String)`: Destination point of the flight.
- `departureTime (String)`: Scheduled departure time.
- `capacity (int)`: Total number of seats available on the flight.
- `numberOfSeatsLeft (int)`: Seats remaining for booking.
- `originalPrice (double)`: Base price of a ticket.

**Functionality**:
- Constructor for initializing flight details.
- Getters and setters for managing flight attributes.
- `bookASeat()`: Books a seat if available and updates seat count.

### 2. Passenger (Abstract Class)
**Common Attributes**:
- `name (String)`: Name of the passenger.
- `age (int)`: Age of the passenger.

### 3. Member (Subclass of Passenger)
**Additional Attribute**:
- `yearsOfMembership (int)`: Duration of membership in years.

**Functionality**:
- Overrides `applyDiscount(double p)`: Provides a discount based on years of membership.

### 4. NonMember (Subclass of Passenger)
**Functionality**:
- Overrides `applyDiscount(double p)`: Provides a discount based on the age of the passenger.

### 5. Ticket
**Attributes**:
- `passenger (Passenger)`: The passenger holding the ticket.
- `flight (Flight)`: Flight details.
- `price (double)`: Ticket price after applicable discounts.
- `number (int)`: Unique ticket identifier.

### 6. Manager
**Functionality**:
- `createFlights()`: Initializes flights based on user input.
- `displayAvailableFlights(String origin, String destination)`: Lists available flights between specified locations.
- `getFlight(int flightNumber)`: Retrieves details of a specific flight.
- `bookSeat(int flightNumber, Passenger passenger)`: Books a seat on a flight and issues a ticket with applicable discounts.

## Usage
To interact with the system:
1. Compile all Java files.
2. Run the `Manager` class to initiate the application, allowing you to create flights and manage bookings.

## Testing
**Unit Testing**:
- Includes JUnit 4 tests for the `Flight` class, covering constructors, getters, setters, the `bookASeat()` method, and the `toString()` method.

