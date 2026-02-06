# lockcheck-initial

# Lock checking system (prototype)
This project is a simple prototype of the lock checking system

The goal of this project is to simulate how a locker can be locked and unlocked digitally. It foucuses on backend logic, API design and basic frontend interation.
It might be used for further software development.

# what does this project do

In this system:

- A locker system contains multiple lockers, each one is resposible for lockinhg a box
- Each box has a status:
  - 'Avaliable' - lock is free to use
  - 'Locked' - reserved for a user
  - 'Occupied' - currently in use
    
- User can:
  - View all time slot
  - Lock an avilable slot
  - Unlock a locked slot (if it is owned by the user)

- A locked slot can be automactically released after a timeout (*)

Further feature can be considered:
- Scan QR code to link the application
- Map to locate the locker

# Reasons for this project

This project is built to:

- Practice C# and ASP.NET Core
- Learn REST API Design
- Simulate a real-world system

# Tech Stack

## Backend
- C#
- ASP.NET Core Web API
- Entity Framework Core
- SQLite (development only)

## Frontend
- simple web frontend (VUE/REACT)
- REST API communication using HTTP

*might migrate to phone application for further development

## Basic System Flow

1. 
