# Task Management System

A web-based task and project management application built with **ASP.NET Core MVC, C#, Entity Framework Core, and SQL Server**.

## Overview

The Task Management System is designed to organize tasks and projects in one place. It includes task-related information such as status, priority, due dates, and project associations, with a database-backed architecture.

## Tech Stack

- **Backend:** C#, ASP.NET Core MVC, .NET 8
- **Database:** Microsoft SQL Server
- **ORM:** Entity Framework Core
- **Frontend:** HTML, CSS, JavaScript, Bootstrap
- **Tools:** Visual Studio Code, Git, GitHub

## Features

- Task and project management structure
- Task status and priority tracking
- Due-date and task-description fields
- SQL Server database integration
- Entity Framework Core migrations
- MVC architecture with separate Models, Views, and Controllers
- Responsive UI built with Bootstrap

> Note: Feature availability depends on the current implementation. Verify task creation, editing, deletion, search, and filtering before claiming them as fully working.

## Project Structure

```text
Task-Management-System/
├── Controllers/
├── Data/
├── Migrations/
├── Models/
├── Properties/
├── Views/
├── wwwroot/
├── CapstoneTask.csproj
├── Program.cs
├── appsettings.json
└── .gitignore
```

## Getting Started

### Prerequisites

- .NET 8 SDK
- Microsoft SQL Server
- Git

### 1. Clone the repository

```bash
git clone https://github.com/rishupandey80/Task-Management-System.git
cd Task-Management-System
```

### 2. Configure the database

Update the `ConnectionStrings:DefaultConnection` value in `appsettings.json` for your SQL Server instance.

Example for SQL Server Express:

```json
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost\\SQLEXPRESS;Database=CapstoneTaskDB;Trusted_Connection=True;TrustServerCertificate=True;MultipleActiveResultSets=true"
  }
}
```

Use your own SQL Server instance details. Do not commit passwords or other sensitive credentials.

### 3. Restore dependencies

```bash
dotnet restore
```

### 4. Apply database migrations

```bash
dotnet ef database update
```

If the Entity Framework CLI tool is not installed, install the version compatible with EF Core 8:

```bash
dotnet tool install --global dotnet-ef --version 8.0.0
```

### 5. Run the application

```bash
dotnet run
```

Open the local URL shown in the terminal. The Tasks page is available at `/Tasks`.

## Database

The application uses Entity Framework Core to manage its SQL Server database. The current migration defines the following tables:

- `Tasks`
- `Projects`
- `Users`

## Future Improvements

- Complete and test task creation and editing workflows
- Add authentication and role-based authorization
- Improve validation and error handling
- Add automated unit and integration tests
- Publish a hosted demo

## Author

**Rishu Pandey**

GitHub: [@rishupandey80](https://github.com/rishupandey80)

---

*Built as a project to practice ASP.NET Core MVC, relational database integration, and application development.*
