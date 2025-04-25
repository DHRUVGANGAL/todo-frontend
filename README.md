# Todo App with Authentication

A simple Todo application with user authentication that connects to a backend API.

## Features

- User registration and login
- Create, read, update, and delete todos
- Mark todos as complete/incomplete
- Responsive design with dark mode support

## Project Structure

```
project-root/
├── index.html       # Signup page
├── signin.html      # Login page
├── todo.html        # Todo list page
├── vercel.json      # Vercel configuration
└── README.md        # This file
```

## Backend API

This frontend connects to a serverless API deployed at:
`https://todo-backend-smoky-psi.vercel.app`

## Deployment Instructions

### Deploy to Vercel

1. **Using the Vercel Dashboard:**
   - Sign up or log in to [Vercel](https://vercel.com)
   - Click "New Project"
   - Import your repository from GitHub, GitLab, or Bitbucket
   - Click "Deploy"

2. **Using the Vercel CLI:**
   - Install the Vercel CLI: `npm install -g vercel`
   - Navigate to your project directory
   - Run `vercel login` and follow the prompts
   - Run `vercel` to deploy
   - Run `vercel --prod` to deploy to production

## Local Development

To run the app locally:

1. Clone this repository
2. Open the project folder
3. Open `index.html` in your browser or use a local development server:
   - `npx serve` (if you have Node.js installed)
   - VS Code's Live Server extension
   - Python's SimpleHTTPServer: `python -m SimpleHTTPServer 8000`

## User Flow

1. Users sign up on the index.html page
2. After successful signup, they are redirected to signin.html
3. After signing in, they are redirected to todo.html
4. The token is stored in localStorage for authentication
5. Users can log out by clicking the Logout button

## Notes

- This application uses the browser's localStorage to store the authentication token
- The app will redirect to the login page if the token is missing or invalid
- API errors are displayed as alerts to the user