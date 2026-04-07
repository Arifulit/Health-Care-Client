# PH Health Care

![Next.js](https://img.shields.io/badge/Next.js-16-black)
![React](https://img.shields.io/badge/React-19-149ECA)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-4-06B6D4)
![ESLint](https://img.shields.io/badge/ESLint-9-4B32C3)

A modern healthcare management frontend built with Next.js, TypeScript, and a modular component architecture.

This project focuses on building a scalable and maintainable patient-doctor-admin workflow with dashboard experiences, authentication flows, AI-related service integration hooks, and role-based module organization.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Core Features](#core-features)
3. [Tech Stack](#tech-stack)
4. [Project Structure](#project-structure)
5. [Getting Started](#getting-started)
6. [Available Scripts](#available-scripts)
7. [Environment Variables](#environment-variables)
8. [Code Quality](#code-quality)
9. [Screenshots](#screenshots)
10. [API Documentation](#api-documentation)
11. [Deployment](#deployment)
12. [Roadmap and Tasks](#roadmap-and-tasks)

## Project Overview

PH Health Care is a web application designed to support healthcare operations through a clean, modular frontend architecture.

The codebase is organized around domain-driven modules, reusable UI primitives, typed service layers, and Zod validation schemas, making it suitable for long-term product growth.

## Core Features

- Role-oriented dashboard layout architecture
- Authentication flows (login, register, forgot/reset password, change password)
- Typed API service layer for admin, doctor, patient, payment, and AI modules
- Reusable shared components and UI building blocks
- Zod-based schema validation for forms and domain entities
- Utility hooks for auth token handling and input behavior
- Error, loading, and not-found pages with App Router conventions

## Tech Stack

- Framework: Next.js 16 (App Router)
- Language: TypeScript
- UI: React 19, Tailwind CSS 4, Radix UI components
- Validation: Zod
- Charts/Visuals: Recharts
- Notifications: Sonner
- Linting: ESLint 9 + Next.js config

## Project Structure

```text
src/
	app/                # Route segments, layouts, pages, error/loading states
	components/         # Shared and module-specific UI components
	services/           # API communication by domain (auth/admin/doctor/patient/...)
	hooks/              # Reusable React hooks
	lib/                # Utilities, config, formatting, auth helpers
	types/              # TypeScript interfaces and shared type definitions
	zod/                # Input and entity validation schemas
	assets/             # Project assets (icons/images/svg)
```

## Getting Started

### Prerequisites

- Node.js 20+
- npm 10+

### Installation

```bash
npm install
```

### Run Development Server

```bash
npm run dev
```

Open http://localhost:3000 in your browser.

## Available Scripts

- `npm run dev`: Start local development server
- `npm run build`: Create a production build
- `npm run start`: Run production server from build output
- `npm run lint`: Run ESLint checks

## Environment Variables

Create a `.env` file at the project root and add the variables your API/services require.

Example template:

```env
NEXT_PUBLIC_API_BASE_URL=https://api.example.com
NEXT_PUBLIC_APP_NAME=PH Health Care
```

Adjust names based on your backend contract and service implementation.

## Code Quality

Before creating a pull request, run:

```bash
npm run lint
npm run build
```

This helps ensure linting, typing, and production compilation stay healthy.

## Screenshots

Add product screenshots to make the repository presentation stronger.

Recommended screenshot files:

- public/screenshots/home-page.png
- public/screenshots/dashboard-page.png
- public/screenshots/doctor-list-page.png

Example markdown snippet:

```md
![Home Page](public/screenshots/home-page.png)
![Dashboard](public/screenshots/dashboard-page.png)
![Doctor List](public/screenshots/doctor-list-page.png)
```

## API Documentation

This frontend consumes domain-based service modules from:

- src/services/auth
- src/services/admin
- src/services/doctor
- src/services/patient
- src/services/payment
- src/services/ai

Current API documentation status:

- Planned task reference: Tasks/17. TASK_15_API_DOCUMENTATION.md (inside the Tasks directory)
- Recommended docs format: OpenAPI (Swagger) + Postman Collection
- Suggested sections: Auth, User Roles, Doctors, Patients, Appointments, Payments, AI endpoints

If backend API docs are published, include links here:

- Swagger UI: https://your-api-domain.com/docs
- Postman Collection: https://www.postman.com/your-workspace/your-collection

## Deployment

This app can be deployed to any platform that supports Next.js (for example, Vercel, Netlify, or self-hosted Node environments).

Recommended production flow:

1. Configure environment variables.
2. Build with `npm run build`.
3. Start with `npm run start`.

## Roadmap and Tasks

The repository contains a structured implementation roadmap under the `Tasks/` directory, including advanced modules such as:

- WebSocket notifications
- Video consultation
- Chat system
- Redis caching
- MFA and security audit tasks
- Testing and CI/CD planning
- API documentation and monitoring

These documents can be used as a guided execution plan for incremental delivery.
