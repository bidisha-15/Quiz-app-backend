# Quiz-app-backend

Welcome to the backend repository of the **Quiz Website**. This backend handles user management, quiz creation, quiz-taking functionality, and result processing. It serves as the backbone for the quiz platform, ensuring secure and efficient data handling.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [API Endpoints](#api-endpoints)
- [License](#license)

---

## Features

- **User Authentication**: Register and log in users with secure password hashing.
- **Quiz Management**: Create, edit, delete, and list quizzes.
- **Question Management**: Add, update, and delete questions within a quiz.
- **Quiz Taking**: Submit answers and get scores in real-time.
- **Result Analysis**: Track and retrieve performance data for users.
- **Role-Based Access**: Admin and user roles with specific permissions.

---

## Technologies Used

- **Framework**: Node.js with Express.js
- **Database**: MongoDB
- **Authentication**: JSON Web Tokens (JWT)
- **Validation**: Joi for input validation
- **Others**: 
  - bcrypt.js for password hashing
  - dotenv for environment variable management

---

## Installation

1. Clone the repository:


   git clone https://github.com/your-username/quiz-website-backend.git
   cd quiz-website-backend


2. Install dependencies:


   npm install
   

3. Set up the environment variables (see [Environment Variables](#environment-variables)).

4. Start the development server:

  
   npm run dev
   

---

## Environment Variables

Create a `.env` file in the root directory and add the following variables:


PORT=5000
MONGO_URI=<your-mongodb-uri>
JWT_SECRET=<your-secret-key>
NODE_ENV=development


Replace placeholders with your values.

---

## API Endpoints

### **Authentication**

- **POST** `/api/auth/register`  
  _Register a new user._

- **POST** `/api/auth/login`  
  _Log in a user and retrieve a token._

---

### **Quizzes**

- **GET** `/api/quizzes`  
  _Get a list of all quizzes._

- **POST** `/api/quizzes`  
  _Create a new quiz._  
  _Admin-only._

- **PUT** `/api/quizzes/:id`  
  _Update an existing quiz._  
  _Admin-only._

- **DELETE** `/api/quizzes/:id`  
  _Delete a quiz._  
  _Admin-only._

---

### **Questions**

- **POST** `/api/quizzes/:quizId/questions`  
  _Add a question to a quiz._  
  _Admin-only._

- **PUT** `/api/questions/:id`  
  _Update a question._  
  _Admin-only._

- **DELETE** `/api/questions/:id`  
  _Delete a question._  
  _Admin-only._

---

### **Quiz-Taking**

- **POST** `/api/quizzes/:quizId/submit`  
  _Submit answers for a quiz and receive the result._

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to contribute or report issues in the [issues section](https://github.com/bidisha-15/Quiz-app-backend/issues).
