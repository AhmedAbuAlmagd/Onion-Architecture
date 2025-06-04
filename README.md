#  Onion Architecture Example

## 📋 Overview
This project demonstrates the implementation of Onion Architecture in a .NET application. The architecture promotes a clean separation of concerns and dependency inversion principles.

## 🏗️ Architecture Layers

### 🎯 Core Domain Layer
- Contains the business entities and business logic
- Independent of any other layers
- No dependencies on external frameworks or libraries

### 🔄 Application Layer
- Contains application business rules
- Orchestrates the flow of data to and from the domain entities
- Implements use cases that the application is meant to perform

### 🔌 Infrastructure Layer
- Implements interfaces defined in the application layer
- Contains external concerns like:
  - Database access
  - File system operations
  - External API calls
  - Email services

### 🌐 Presentation Layer
- Handles user interface concerns
- Can be implemented as:
  - Web API
  - Console application
  - Desktop application
  - Mobile application

## 🚀 Key Features
- ✅ Clean separation of concerns
- ✅ Dependency Inversion Principle
- ✅ Testable business logic
- ✅ Flexible and maintainable codebase


## 🛠️ Technologies Used
- .NET Core
- Entity Framework Core
- SQL Server
- C#

## 📁 Project Structure
```
SystemSolution/
│
├── System.API/                 --> 💻 Presentation Layer
│   ├── Controllers/              --> API endpoints (EmployeeController, LeaveController, etc.)
│   ├── Filters/                  --> Custom filters (e.g., Exception handling)
│   ├── Middlewares/             --> Auth, logging, error-handling middlewares
│   └── Program.cs / Startup.cs  --> App entry point & dependency injection
│
├── System.Application/         --> 📦 Application Layer (Use Cases)
│   ├── Interfaces/               --> Service contracts (IEmployeeService, ILeaveService)
│   ├── Services/                 --> Application logic that uses Domain + Infra
│   ├── DTOs/                     --> Data Transfer Objects (EmployeeDto, LeaveDto)
│   ├── Validators/               --> FluentValidation classes for DTOs
│   └── Common/                   --> Shared helpers, constants, enums, etc.
│
├── HRSystem.Domain/              --> 🧠 Domain Layer (Core Business Rules)
│   ├── Entities/                 --> Domain models (Employee, LeaveRequest, etc.)
│   ├── ValueObjects/            --> Immutable objects (e.g., Email, Address)
│   ├── Interfaces/              --> Abstractions (e.g., IEmployeeRepository)
│   ├── Enums/                   --> Domain enums (LeaveType, Gender, etc.)
│   └── Exceptions/              --> Domain-specific custom exceptions
│
├── HRSystem.Infrastructure/      --> 🏗️ Infrastructure Layer (DB, File, Email)
│   ├── Persistence/              --> EF Core DbContext, Migrations
│   │   ├── HrDbContext.cs        --> EF Core context (unit of work)
│   │   ├── Migrations/           --> EF Core migrations
│   │   └── SeedData.cs           --> Optional: Seed initial data
│   ├── Repositories/            --> EF implementations (EmployeeRepository, etc.)
│   ├── Services/                --> Infra services (EmailService, FileUploader)
│   └── Configurations/         --> Fluent API entity configs (if needed)
│
│
└── HRSystem.sln                  --> 🔗 Visual Studio solution file

```

## 🎯 Benefits
- 🔄 Easy to maintain and modify
- 🧪 Simplified testing
- 🔌 Flexible infrastructure changes
- 🎨 Clear separation of concerns
- 📈 Scalable architecture

