# Overview

TaxiPro is a modern taxi booking platform built as a full-stack web application. The system serves both customers who need transportation and drivers who provide taxi services. It features real-time communication through WebSockets, allowing for instant updates on booking requests, driver availability, and trip status changes. The application provides separate interfaces for clients to book rides and drivers to manage their availability and accept trip requests.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **Styling**: Tailwind CSS with shadcn/ui component library for consistent UI components
- **State Management**: React Query (TanStack Query) for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation for type-safe form management
- **Real-time Updates**: Custom WebSocket hook for live data synchronization

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript for type safety across the entire application
- **Real-time Communication**: WebSocket server for instant notifications and updates
- **API Design**: RESTful API with dedicated routes for drivers and bookings
- **Data Validation**: Zod schemas shared between frontend and backend for consistent validation

## Database and Data Management
- **Database**: PostgreSQL using Neon serverless database
- **ORM**: Drizzle ORM for type-safe database queries and migrations
- **Schema Management**: Shared TypeScript schemas between client and server for data consistency
- **Connection Pooling**: Connection pooling through Neon's serverless architecture

## Core Data Models
- **Drivers**: Profile information, vehicle details, online status, and ratings
- **Bookings**: Trip requests with pickup/dropoff locations, client details, and status tracking
- **Users**: Basic user management (prepared for future authentication features)

## Key Features
- **Dual Interface System**: Separate optimized interfaces for clients and drivers
- **Real-time Updates**: Live status changes for bookings and driver availability
- **Driver Management**: Registration, online/offline status toggling, and trip acceptance
- **Booking Lifecycle**: Complete flow from trip request to completion with status tracking
- **Responsive Design**: Mobile-first approach with responsive components

## Development and Deployment
- **Development Server**: Vite dev server with Express API integration
- **Build Process**: Optimized builds for both frontend and backend
- **Environment Configuration**: Proper separation of development and production settings
- **Code Organization**: Clean separation between client, server, and shared code

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL database with WebSocket support for real-time features

## UI and Styling Libraries
- **Radix UI**: Accessible component primitives for building the user interface
- **Tailwind CSS**: Utility-first CSS framework for styling
- **shadcn/ui**: Pre-built component library built on Radix UI and Tailwind

## Frontend Libraries
- **React Query**: Server state management and caching
- **React Hook Form**: Form handling and validation
- **Wouter**: Lightweight routing library
- **Embla Carousel**: Carousel component for enhanced UI

## Backend Libraries
- **Express.js**: Web application framework
- **WebSocket (ws)**: Real-time bidirectional communication
- **Drizzle ORM**: TypeScript ORM for database operations

## Development Tools
- **Vite**: Build tool and development server
- **TypeScript**: Type safety across the application
- **ESBuild**: Fast JavaScript bundler for production builds