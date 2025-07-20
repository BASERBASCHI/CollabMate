# CollabMate - Team Collaboration Platform

## Overview
A React-based collaboration platform that helps students and developers find teammates and work on projects together. The application features Firebase authentication, real-time messaging, AI-powered user matching, and project suggestions using Google's Generative AI.

## Recent Changes
- **Complete Team Collaboration System** (July 20, 2025)
  - Fixed critical profile navigation bug - clicking on user profiles now shows correct user instead of current user
  - Added comprehensive team creation and management system with CreateTeam.tsx component
  - Built TeamsView.tsx with team discovery, filtering, and joining functionality
  - Implemented full team API backend with GET /api/teams, POST /api/teams, and POST /api/teams/:teamId/join
  - Added team database schema with teams and teamMembers tables
  - Created sample teams (AI Study Assistant, Campus Sustainability Tracker) for demonstration
  - Enhanced navigation system to support teams and create-team views
  - Updated Profile component to handle viewing other users' profiles vs current user
  - Added "View Teams" and "Create Team" buttons in sidebar for easy access
  - App now functions as a full-fledged collaboration platform with real user matching and team formation

- **Real User Integration Complete** (July 19, 2025)
  - Successfully integrated real Firebase users with PostgreSQL database
  - Added /api/users endpoint to fetch all users from database
  - Updated useApiUsers hook to display real users instead of mock data
  - Fixed Express route ordering issue (moved /api/users before /api/users/:id)
  - Added sample users to database for demonstration (Sarah Chen, Alex Rodriguez, Maria Garcia, David Kim)
  - Updated matching system to generate matches based on real user data and skills
  - Users can now see actual profiles with real skills for collaboration matching

- **Database Integration** (July 19, 2025)
  - Added PostgreSQL database with comprehensive Drizzle ORM schema
  - Created tables for users, projects, matches, messages, teams, and team members
  - Built complete API routes for all CRUD operations
  - Integrated Firebase authentication with database sync via /api/sync-user endpoint
  - Updated profile update functionality to use database instead of Firebase

- **Migration from Bolt to Replit** (July 19, 2025)
  - Installed Firebase and Google Generative AI dependencies
  - Fixed import path issues for TypeScript types 
  - Cleaned up duplicate fields in type definitions
  - Implemented missing `updateUserProfile` function in useFirebaseAuth hook
  - Fixed profile completion functionality

## Project Architecture
- **Frontend**: React + TypeScript + Vite
- **Backend**: Express.js server with Firebase integration
- **Database**: PostgreSQL with Drizzle ORM for data persistence, Firebase Auth for authentication
- **Authentication**: Firebase Auth with Google login support, synced with PostgreSQL database
- **AI Integration**: Google Generative AI for chat suggestions and project recommendations
- **Styling**: Tailwind CSS with custom components
- **Data Flow**: Firebase Auth → Database Sync API → PostgreSQL → Frontend

## Key Features
- User authentication (email/password and Google login) with Firebase integration
- Real-time user matching based on skills and preferences using real database users
- Complete team creation and management system with project-based collaboration
- Team discovery with filtering (All Teams, Available Teams, My Teams)
- Team joining functionality with member limits and role management
- Profile viewing system that correctly displays other users' profiles
- Chat messaging with AI-powered suggestions
- Profile completion system with strength scoring
- Project suggestions based on user skills
- Dashboard with matches and project recommendations
- Full PostgreSQL database integration with persistent data storage

## User Preferences
- User prefers complete, working solutions over partial implementations
- Focus on real-time functionality and Firebase integration
- Maintain clean code structure with proper TypeScript typing

## Technical Details
- Server runs on port 5000 with both API and frontend
- Uses Firebase SDK v9+ modular imports
- Implements proper client/server separation
- All types defined in shared schema for consistency