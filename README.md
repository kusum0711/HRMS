# Human Resource Management System (Backend)

A backend system for managing Human Resource functions like employee records, leave applications, departments, holidays, and user access control. This project was developed as part of a B.Tech final year project.

> ⚠️ This repository contains only the **backend** built using **NestJS** and **MySQL**. The Angular frontend was developed separately and is not part of this repository.

---

## 📌 Project Overview

The Human Resource Management System (HRMS) backend provides secure REST APIs to support:

- Employee Management
- Department Management
- Leave and Holiday Management
- User and Role Management
- Authentication and Authorization

It follows a modular architecture with scalability, performance, and data integrity in mind.

---

## 🛠️ Tech Stack

- **Backend Framework**: [NestJS](https://nestjs.com/) (Node.js + TypeScript)
- **Frontend Framework**: Not added here
- **Database**: MySQL
- **Authentication**: JWT-based token auth
- **Other Tools**: REST API, TypeORM, bcrypt, dotenv

---

## 🧩 Key Backend Features

- 📂 **Modular Code Structure** using NestJS modules and services
- 🔐 **User Authentication & Authorization** with role-based access control (Admin, HR, Manager, Employee)
- 📄 **CRUD APIs** for Employees, Departments, Leaves, Holidays
- 📆 **Leave Workflow** including approval/rejection flow
- 🧾 **Data Models** aligned with a normalized ER diagram and enforced with validations
- 🧪 **Tested with API testing tools** (Postman)

---

## ⚙️ Setup & Installation

### 📋 Prerequisites

- Node.js (v14+)
- MySQL Server
- npm

### 📦 Installation Steps

```bash
# Clone repository
git clone https://github.com/your-username/hrms-backend.git
cd hrms-backend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Then update DB credentials and secrets inside .env

# Run migrations (if using TypeORM CLI)
npm run typeorm migration:run

# Start development server
npm run start:dev
```

## Directory Structure

```
src/
├── auth/              # JWT authentication logic (login, token)
├── users/             # User entity, roles, and permission handling
├── employees/         # Employee CRUD, personal info, status
├── departments/       # Department creation, assignment, reports
├── leaves/            # Leave requests, approval flow
├── holidays/          # Holiday calendar setup and retrieval
├── common/            # DTOs, guards, interceptors, pipes
├── database/          # TypeORM configuration and DB connection
├── app.module.ts      # Main application module
└── main.ts            # Entry point of the NestJS app
```
