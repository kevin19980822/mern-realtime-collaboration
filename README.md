# Real-Time Collaboration Platform

A TypeScript MERN collaboration workspace with persistent direct/group/channel messaging, Socket.IO live updates, online presence, typing indicators and notifications.

## Stack
React + Vite + TypeScript, Express + TypeScript, MongoDB/Mongoose, Socket.IO, JWT and Zod.

## Setup
Requirements: Node.js 20+ and MongoDB 7+. Copy `.env.example` to `.env`, set a random JWT secret (32+ characters), then run `npm install`, `npm run dev`. Open http://localhost:5175; API runs on port 4002.

## Workflow
Register at least two accounts. Create a conversation or channel and add the other user's email. Open the same conversation in both browser sessions to test real-time messages, presence and typing. Message history is persisted in MongoDB.

## API
POST /api/auth/register, POST /api/auth/login, GET /api/auth/me
GET/POST /api/conversations, GET /api/conversations/:id/messages, POST /api/conversations/:id/messages
GET /api/notifications, PATCH /api/notifications/:id/read

File uploads are not included in this version; the UI intentionally leaves the attachment control disabled until a storage provider and malware-scanning policy are configured. Presence currently uses in-memory state and should use a Redis Socket.IO adapter for multi-instance deployment.\n\nSocket.IO events: conversation:join, message:send, message:new, typing:start, typing:stop, presence:update, conversation:error. Socket access is verified using JWT and conversation membership.

Portfolio project. Before production use add rate limits, moderation/reporting, file storage scanning, message retention policies, observability, backup strategy and security review.
