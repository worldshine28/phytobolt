# Overview

PhytoBolt is a modern, animated environmental awareness website focused on educating users about the critical threat microplastics pose to ocean phytoplankton - the microscopic organisms that produce 50% of Earth's oxygen. Built as a static, presentation-style website for the HackTheOcean 2025 hackathon, it combines storytelling with visual impact to raise awareness about this invisible environmental crisis and inspire action.

The project features a full-screen, slide-like design with oceanic themes, smooth animations, and compelling visual content that guides users through understanding the problem and potential solutions. It's designed to feel like an interactive PowerPoint presentation optimized for judges and environmental advocates.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript in a Vite-powered single-page application
- **Styling**: Tailwind CSS with custom oceanic color scheme (deep blues, cyans, teals) and CSS variables for theming
- **UI Components**: Comprehensive shadcn/ui component library with Radix UI primitives for accessibility
- **Animations**: AOS (Animate on Scroll) library for smooth scroll-triggered animations and transitions
- **Fonts**: Google Fonts integration (Poppins, Inter, Montserrat) for modern typography hierarchy
- **Responsive Design**: Mobile-first approach with scroll-snap effects for presentation-like navigation

## Backend Architecture
- **Server**: Express.js with TypeScript serving as a minimal API layer
- **Development Setup**: Vite development server with hot module replacement and error overlay
- **Build Process**: ESBuild for server bundling and Vite for client build optimization
- **Static Serving**: Express serves the built React application in production

## Data Storage Solutions
- **Database ORM**: Drizzle ORM configured for PostgreSQL with type-safe schema definitions
- **Schema Location**: Shared schema definitions in `/shared/schema.ts` for type consistency
- **Migrations**: Drizzle Kit handles database migrations with PostgreSQL dialect
- **Connection**: Neon Database serverless PostgreSQL configured via environment variables
- **Development Storage**: In-memory storage implementation for development/testing

## Authentication and Authorization
- **Session Management**: PostgreSQL session store using connect-pg-simple
- **User Schema**: Basic user table with username/password fields and UUID primary keys
- **Type Safety**: Zod validation schemas integrated with Drizzle for runtime type checking
- **Authentication Flow**: Server-side session management with cookie-based authentication

## External Dependencies
- **Database**: Neon Database (serverless PostgreSQL) for production data storage
- **Fonts**: Google Fonts CDN for typography (Poppins, Inter, Montserrat families)
- **Animations**: AOS (Animate on Scroll) library loaded via CDN for scroll-triggered animations
- **Development Tools**: Replit integration with cartographer plugin and runtime error modal
- **Build Tools**: Vite build system with React plugin and TypeScript support
- **UI Framework**: Radix UI component primitives for accessible interface elements
- **Utilities**: Class variance authority for component styling variants, clsx for conditional classes