# Real-Time Collaboration Platform

A TypeScript MERN collaboration app foundation for private and group messaging, team channels, presence, notifications, and file sharing.

## Stack
- React + TypeScript client (planned)
- Node.js + Express + TypeScript
- MongoDB + Mongoose
- Socket.IO real-time gateway (planned)
- JWT authentication and Zod validation

## Getting started
1. Install Node.js 20+ and MongoDB.
2. Copy `.env.example` to `.env`.
3. Run `npm install`, then `npm run dev`.

## Current implementation
Initial API foundation with health endpoint and centralized error handling. Authenticated conversations, message persistence, Socket.IO rooms, presence, and React UI are planned for follow-up commits.

## Design considerations
Persist messages before broadcasting; authorize room membership on every socket join; validate payloads; rate-limit message creation; never trust client-provided sender IDs.
