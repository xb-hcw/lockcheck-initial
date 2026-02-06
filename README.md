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
  

## Basic System Flow

1. The frontend requries all slots of each locker from the backend
2. The user choose and click lock on an available slot
3. The backend:
   - Check the slot status
   - Changed it to 'locked'
   - Creates a reservation with an expiration time (*)
4. System will automatically unlock the locker if the slot is not used before the expiration time (with penalty*)

## Example API Endpoints

```http
GET /api/slots
POST /api/slots/{id}/lock
POST /api/slots/{id}/unlock
GET /api/slots/{id}
```

# Project Status

This is an early-stage prototype for the locking system

Planned improvements:

- User Login&Registration (Authentication)
- Concurrency Control
- Real-time updates (Sensor/SignalR)
- Integration with real locker hardware (future)
- Physical Access to the locker
- Scan QR code to link the application
- Map to locate the locker
- payment system
- phone application

* This project focuses on logic and system design, UI might be considered in the future
