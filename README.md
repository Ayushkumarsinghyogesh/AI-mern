# SecureQuiz

SecureQuiz is an online quiz platform with role-based experiences for students,
teachers, and administrators. Teachers can create and upload quizzes, students
can take quizzes, and administrators can manage users and questions.

This repository contains the Angular frontend. The backend source code is
available in the [MERN-stack Quiz repository](https://github.com/Ayushkumarsinghyogesh/Mern-stack-Quiz).

## Features

- Student and teacher authentication
- Password reset flow
- Teacher tools for creating quizzes, adding questions, and viewing students
- Student quiz-taking workflow
- Admin views for managing students, teachers, and questions
- Protected routes for student, teacher, and admin areas
- Webcam and anti-cheating support in the quiz experience
- Real-time communication through Socket.IO

## Technology

- Angular 10
- TypeScript
- RxJS
- Socket.IO Client
- Karma and Jasmine for unit tests
- Protractor for end-to-end tests

## Prerequisites

Install the following before starting:

- Node.js and npm
- Angular CLI 10
- The SecureQuiz backend running locally or at a reachable URL

You can install the matching Angular CLI globally with:

```bash
npm install --global @angular/cli@10
```

## Getting Started

Clone the frontend repository and install its dependencies:

```bash
git clone <frontend-repository-url>
cd SecureQuiz-master/quiz
npm install
```

Start the development server:

```bash
npm start
```

Open [http://localhost:4200](http://localhost:4200) in your browser. The
development server reloads the application when source files change.

Start the backend separately using the instructions in the
[backend repository](https://github.com/Ayushkumarsinghyogesh/Mern-stack-Quiz),
then confirm that the frontend environment configuration points to the correct
backend URL.

## Available Scripts

Run these commands from the `quiz` directory:

| Command | Description |
| --- | --- |
| `npm start` | Start the Angular development server |
| `npm run build` | Create a production build |
| `npm test` | Run unit tests with Karma |
| `npm run lint` | Run the TSLint checks |
| `npm run e2e` | Run end-to-end tests |

## Main User Areas

- `/student` - Student login
- `/teacher` - Teacher login
- `/admin/adminhome` - Admin dashboard

Additional routes are protected by role-specific route guards and require a
running backend with valid authentication data.

## Project Structure

```text
quiz/
├── src/app/auth/       Authentication and password reset
├── src/app/student/    Student dashboard and quiz taking
├── src/app/teacher/    Quiz creation and teacher tools
├── src/app/admin/      Administrative views
├── src/app/services/   API, authentication, and WebSocket services
└── src/environments/   Environment-specific configuration
```

## Production Build

Build the application for deployment with:

```bash
npm run build
```

The compiled files are written to the Angular `dist/` directory.

## License

No license has been specified for this project.