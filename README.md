# Next.js Authentication and User Management Project

This is a full-stack Next.js application implementing authentication features such as signup, login, password reset, email verification, and Google authentication using Next Auth. The project uses TypeScript, Tailwind CSS, and a MongoDB database.

![Entry Page](image-2.png)
![DashBoard](image.png)
![History](image-1.png)

## Project Structure
```
├── src
│   ├── app
│   │   ├── api
│   │   │   ├── auth
│   │   │   │   └── [...nextauth]
│   │   │   │       └── route.js
│   │   │   └── users
│   │   │       ├── forgot-password
│   │   │       │   └── route.ts
│   │   │       ├── history
│   │   │       │   └── route.js
│   │   │       ├── history_fetch
│   │   │       │   └── route.js
│   │   │       ├── login
│   │   │       │   └── route.ts
│   │   │       ├── logout
│   │   │       │   └── route.ts
│   │   │       ├── me
│   │   │       │   └── route.ts
│   │   │       ├── otp
│   │   │       │   └── route.js
│   │   │       ├── reset-password
│   │   │       │   └── route.ts
│   │   │       ├── search
│   │   │       │   └── route.js
│   │   │       ├── signup
│   │   │       │   └── route.ts
│   │   │       ├── verifyemail
│   │   │       │   └── route.ts
│   │   │       └── verify-otp
│   │   │           └── route.ts
│   │   ├── Backtrack_to_History
│   │   │   └── [companyName]
│   │   │       └── page.jsx
│   │   ├── favicon.ico
│   │   ├── forgot-password
│   │   │   └── page.tsx
│   │   ├── globals.css
│   │   ├── histemp
│   │   │   └── [companyName]
│   │   │       └── page.jsx
│   │   ├── layout.tsx
│   │   ├── login
│   │   │   └── page.tsx
│   │   ├── page.tsx
│   │   ├── profile
│   │   │   ├── [id]
│   │   │   │   └── page.tsx
│   │   │   └── page.tsx
│   │   ├── reset-password
│   │   │   └── page.jsx
│   │   ├── search
│   │   │   └── page.tsx
│   │   ├── searchtemp
│   │   │   └── page.tsx
│   │   ├── signup
│   │   │   └── page.tsx
│   │   ├── verifyemail
│   │   │   └── page.tsx
│   │   └── verify-otp
│   │       └── page.tsx
│   ├── components
│   │   ├── compo
│   │   │   └── history.jsx
│   │   ├── graphs
│   │   │   ├── diversity.jsx
│   │   │   ├── expense2024.jsx
│   │   │   ├── expense.jsx
│   │   │   ├── globalstock.jsx
│   │   │   ├── market2024.jsx
│   │   │   ├── market.jsx
│   │   │   ├── revenue2024.jsx
│   │   │   ├── revenue.jsx
│   │   │   ├── stock2024.jsx
│   │   │   └── stock.jsx
│   │   ├── search.module.css
│   │   ├── SessionProviderWrapper.tsx
│   │   └── ui
│   │       ├── progress.tsx
│   │       └── skeleton.tsx
│   ├── dbConfig
│   │   └── dbConfig.ts
│   ├── helpers
│   │   ├── getDataFromToken.ts
│   │   ├── mailer-reset.ts
│   │   ├── mailer.ts
│   │   ├── otp_mail.ts
│   │   └── searchableDrop.js
│   ├── lib
│   │   └── utils.ts
│   ├── middleware.ts
│   └── models
│       ├── companyModel.js
│       ├── HistoryModel.js
│       └── userModel.js

```
## Features

- **Authentication**: User authentication with support for Google OAuth via Next Auth.
- **Signup/Login**: Users can register and log in with email and password.
- **Password Reset**: Forgot password and reset password functionality using email verification.
- **Profile Management**: Users can view and edit their profiles.
- **JWT Token**: Authentication tokens are used to secure API routes.
- **Email Verification**: Email verification is required for signup and password recovery.
- **Tailwind CSS**: Styling is handled with Tailwind for utility-first CSS.

## Prerequisites

- **Node.js** (v16 or above)
- **MongoDB**: A running MongoDB instance for the database
- **Google OAuth**: A Google Developer account for setting up OAuth

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```
### 2. Install dependencies
```bash
npm install
```
### 3. Setup environment variables
- Create a .env.local file in the root directory and configure the following environment variables:

```bash
NEXTAUTH_URL=http://localhost:3000
MONGODB_URI=mongodb+srv://<username>:<password>@cluster0.mongodb.net/mydatabase
JWT_SECRET=your-jwt-secret
GOOGLE_CLIENT_ID=your-google-client-id
GOOGLE_CLIENT_SECRET=your-google-client-secret
```
### 4. Run the development server

```bash
npm run dev
```

### API Endpoints
- POST /api/users/signup: Register a new user
- POST /api/users/login: Login with email and password
- POST /api/users/logout: Logout the current user
- GET /api/users/me: Fetch the current user's profile
- POST /api/users/forgot-password: Request a password reset link
- POST /api/users/reset-password: Reset the user's password
- POST /api/users/verifyemail: Verify the user's email address

### How to Contribute
- Fork the project
- Create your feature branch: git checkout -b feature/my-feature
- Commit your changes: git commit -m 'Add some feature'
- Push to the branch: git push origin feature/my-feature
- Open a pull request

### License
- This project is licensed under the MIT License. See the LICENSE file for more details.

