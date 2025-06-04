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
src/
├── Core/                 # Domain entities and interfaces
├── Application/         # Application business rules
├── Infrastructure/      # External concerns implementation
└── API/        # API endpoints and controllers
```

## 🎯 Benefits
- 🔄 Easy to maintain and modify
- 🧪 Simplified testing
- 🔌 Flexible infrastructure changes
- 🎨 Clear separation of concerns
- 📈 Scalable architecture

