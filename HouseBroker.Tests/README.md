# HouseBrokerApp

## Project Overview
HouseBrokerApp is a Minimum Viable Product (MVP) for a House Broker Application built using .NET 8, MSSQL, and Clean Architecture principles. It enables brokers to manage property listings and seekers to search for properties efficiently.

## Architecture
The solution follows Clean Architecture:
- **Domain**: Core business logic and entities (Property, User, Commission).
- **Application**: Interfaces, DTOs, and services for business operations.
- **Infrastructure**: Database access (EF Core), repositories, caching.
- **WebAPI**: Controllers exposing RESTful endpoints for authentication, listings, and search.

## Features
- User authentication with .NET Identity (roles: Broker, HouseSeeker).
- CRUD operations for property listings with validation and caching.
- Commission engine configurable via database.
- Search and filter functionality for properties.
- API endpoints for third-party integration.

## Tech Stack
- .NET 8
- MSSQL
- EF Core
- Caching (in-memory or distributed)

## Setup Instructions
### Prerequisites
- Install [.NET SDK](https://dotnet.microsoft.com/download)
- Install MSSQL Server and configure a database.

### Steps
1. Clone the repository.
2. Update the connection string in `Infrastructure/Persistence/AppDbContext.cs`.
3. Run EF Core migrations:
   ```bash
   dotnet ef database update
   ```
4. Start the WebAPI project:
   ```bash
   dotnet run --project WebAPI
   ```

## Testing
Run unit tests using:
```bash
dotnet test
```

## Folder Structure
```
HouseBrokerApp/
├── Domain/
├── Application/
├── Infrastructure/
├── WebAPI/
└── Tests/
```

