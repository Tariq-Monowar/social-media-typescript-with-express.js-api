# social media express.js api with typescript
This repository contains the backend code for a social media platform built with Express.js. The backend provides APIs for user management, posts, friendships, comments, infinite comment replies with media, logical reactions (like, love, care, etc.), notifications, and more
#### User Routes
- `POST /users/register` - Register a new user
- `POST /users/verify-otp` - Verify OTP for registration
- `POST /users/login` - User login
- `PATCH /users/update-profile` - Update user profile (requires authentication)
- `POST /users/verify-password` - Verify user password (requires authentication)
- `POST /users/request-email-update-otp` - Request OTP for email update (requires authentication)
- `PATCH /users/confirm-email-update` - Confirm email update (requires authentication)
- `POST /users/request-forgot-password-otp` - Request OTP for forgot password (requires authentication)
- `POST /users/match-password-otp` - Match OTP for password reset (requires authentication)
- `PATCH /users/reset-forgot-password` - Reset password using OTP (requires authentication)

#### Friend Routes
- `POST /friends/send-request` - Send friend request (requires authentication)
- `POST /friends/reject-request` - Reject friend request (requires authentication)
- `POST /friends/accept-request` - Accept friend request (requires authentication)
- `POST /friends/un-friend` - Unfriend a user (requires authentication)
- `GET /friends/friends-list` - Get friends list (requires authentication)
- `GET /friends/sent-requests` - Get sent friend requests (requires authentication)
- `GET /friends/friend-request` - Get friend requests (requires authentication)
- `GET /friends/friend` - Get a specific friend's details (requires authentication)

#### Post Routes
- `GET /post` - Get all posts
- `GET /post/:postId` - Get a single post by ID
- `POST /post` - Create a new post (requires authentication)
- `PATCH /post/:postId` - Update a post by ID (requires authentication)
- `DELETE /post/:postId` - Delete a post by ID (requires authentication)
- `PATCH /post/reactions/:postId` - React to a post (requires authentication)

#### Comment Routes
- `POST /comment/:postId` - Create a new comment on a post (requires authentication)
- `PATCH /comment/:commentId` - Update a comment by ID (requires authentication)
- `DELETE /comment/:commentId` - Delete a comment by ID (requires authentication)
- `PATCH /comment/reactions/:commentId` - React to a comment (requires authentication)

#### Notification Routes
- `GET /notification` - Get all notifications (requires authentication)
- `DELETE /notification/delete/:id` - Delete a notification by ID (requires authentication)

## Installation
1. Clone the repository:
   ```bash
   git clo
   git clone https://github.com/Tariq-Monowar/social-media-typescript-with-express.js-api.git
2. Install dependencies:
    ```bash
    cd social-media-backend
    npm install
3. Set up environment variables:
   ```bash
   PORT=1010
   DBURL= Mongodb url
   WEBTOKEN_SECRET_KEY=****************
   NODE_MAILER_USER=***********************
   NODE_MAILER_PASSWORD=*********************
   SESSION_SECRET=****************
   CLOUD_NAME=***************
   CLOUD_API_KEY=*******************
   CLOUD_API_SECRET=*************************

# Folder Structure
```
├── config/
│   ├── cloudinary.config.ts
│   ├── db.ts
│   └── config.ts
├── constants/
│   ├── email_message.ts
│   └── interface.ts
├── controllers/
│   ├── comment.controllers.ts
│   ├── friends.controllers.ts
│   ├── notification.controllers.ts
│   ├── posts.controllers.ts
│   └── users.controllers.ts
├── middleware/
│   └── verifyUser.ts
├── models/
│   ├── comment.models.ts
│   ├── friend.models.ts
│   ├── notification.models.ts
│   ├── post.models.ts
│   └── user.models.ts
├── routes/
│   ├── comment.routes.ts
│   ├── friend.routes.ts
│   ├── notification.routes.ts
│   ├── post.routes.ts
│   └── user.routes.ts
├── util/
│   ├── baseUrl.ts
│   └── fireUploade.ts
├── .env
├── .gitignore
├── README.md
├── app.ts
├── index.ts
├── package-lock.json
├── package.json
├── tsconfig.json
```
