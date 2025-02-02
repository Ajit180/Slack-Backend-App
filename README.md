# Message Slack - Backend

## Overview

Message Slack is a full-stack real-time chat application inspired by Slack. This backend repository handles user authentication, workspaces, channels, real-time messaging, file uploads, and other core functionalities.

## Tech Stack

- **Backend Framework**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ORM)
- **Real-Time Communication**: Socket.IO
- **Cloud Storage**: AWS S3 (Pre-signed URLs for secure file uploads)
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/Postman
- **Caching & Rate Limiting**: Redis (for caching and performance optimization), Express-rate-limit
- **Testing**: Jest for unit testing
- **Deployment**: AWS

---

## Features Implemented

### 1. **User Authentication & Authorization**

- JWT-based authentication with refresh tokens
- Role-based access control (RBAC) for workspace and channel permissions
- Secure password hashing using bcrypt.js

### 2. **Workspace & Channel Management**

- Users can create, join, and leave workspaces
- Each workspace contains multiple channels (public/private)
- Role management (admin, member) for channels and workspaces

### 3. **Real-Time Messaging with Socket.IO**

- Instant messaging across channels using WebSockets
- Event-driven architecture for sending/receiving messages
- Online/offline user status tracking

### 4. **File Uploads & Media Sharing**

- AWS S3 integration for image and document uploads
- Secure pre-signed URLs to prevent unauthorized access
- File preview support for images, PDFs, etc.

### 5. **Message Threads & Replies**

- Support for threaded messages in channels
- Users can reply to a specific message in a conversation

### 6. **Search Functionality**

- Full-text search for messages, users, and channels using MongoDB indexing
- Efficient database querying for faster search results

### 7. **Rate Limiting & Security Enhancements**

- Prevent brute-force attacks with express-rate-limit
- Helmet middleware for secure HTTP headers
- CORS enabled for frontend-backend communication

### 8. **Caching & Performance Optimization**

- Redis caching for frequently accessed data (e.g., workspace details, user profiles)
- MongoDB indexing for optimized queries

### 9. **Payment Integration (Upcoming)**

- Integration with Razorpay for premium workspace subscriptions
- Webhook support for handling payment transactions

---




Create a `.env` file in the root directory and add the following:

```env
PORT=3000
MONGO_URI=your-mongodb-connection-string
JWT_SECRET=your-secret-key
AWS_ACCESS_KEY_ID=your-aws-key
AWS_SECRET_ACCESS_KEY=your-aws-secret
AWS_BUCKET_NAME=your-bucket-name
REDIS_URL=redis://localhost:6379
```

### **4. Start the Server**

```bash
  npm run dev
```

---

## Future Enhancements

- Implement **WebRTC-based voice/video calls**
- Introduce **GraphQL** for efficient API querying
- Improve **workspace analytics & reporting**
- Implement **end-to-end encryption for messages**
- Deploy a **CI/CD pipeline** for automated testing & deployment

---

## Contributing

Feel free to open an issue or submit a pull request if you want to contribute!

---
