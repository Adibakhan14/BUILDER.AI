# AI Website Builder

> AI-powered SaaS platform for generating complete React websites from
> natural-language prompts.

[![MERN](https://img.shields.io/badge/Stack-MERN-3FA037?style=flat-square)](#tech-stack)
[![React](https://img.shields.io/badge/Frontend-React.js-61DAFB?style=flat-square&logo=react&logoColor=black)](#tech-stack)
[![Node.js](https://img.shields.io/badge/Backend-Node.js-339933?style=flat-square&logo=node.js&logoColor=white)](#tech-stack)
[![MongoDB](https://img.shields.io/badge/Database-MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)](#tech-stack)
[![OpenRouter](https://img.shields.io/badge/AI-OpenRouter-111827?style=flat-square)](#tech-stack)

## Overview

AI Website Builder is a full-stack AI SaaS application that allows users
to create complete React websites using simple natural-language prompts.

Instead of starting from an empty project, users describe the website
they want and the AI generates the application step by step. Users can
monitor the generation process in real time and continue improving the
generated website through additional AI prompts or by directly editing
the source code.

The project combines modern full-stack development with AI-powered code
generation, authentication, code editing, and website export/publishing
workflows.

## Features

-   **AI Website Generation** --- Generate complete React websites from
    natural-language prompts.
-   **Step-by-Step Generation** --- Track the AI generation process in
    real time.
-   **AI-Powered Iteration** --- Modify an existing website by providing
    additional prompts.
-   **Manual Code Editing** --- Edit generated source code directly.
-   **User Authentication** --- Secure signup and login functionality.
-   **Project Management** --- Create and manage generated website
    projects.
-   **Website Export** --- Export generated website code for further
    development or deployment.
-   **Publishing Workflow** --- Publish generated websites with a
    streamlined workflow.
-   **REST APIs** --- Backend APIs for authentication, projects, AI
    generation, and application data.
-   **AI Code Reviews** --- CodeRabbit is used during development to
    identify issues and suggest code improvements.

## How It Works

``` text
User Prompt
     │
     ▼
React Frontend
     │
     ▼
Node.js + Express API
     │
     ▼
OpenRouter AI Model
     │
     ▼
AI-Generated React Code
     │
     ├──────────────► Real-Time Generation Progress
     │
     ▼
Project Workspace
     │
     ├── AI Prompt ─────► Modify Website
     │
     ├── Code Editor ───► Manual Changes
     │
     └── Export/Publish ─► Final Website
```

## Tech Stack

### Frontend

-   React.js
-   JavaScript
-   HTML5
-   CSS3
-   Code editor integration

### Backend

-   Node.js
-   Express.js
-   REST APIs

### Database

-   MongoDB

### AI

-   OpenRouter
-   LLM-based code generation
-   Prompt engineering

### Development & Code Quality

-   Git & GitHub
-   CodeRabbit

## Project Architecture

The application follows a modular full-stack architecture:

``` text
AI-Website-Builder/
│
├── client/                  # React frontend
│   ├── components/          # Reusable UI components
│   ├── pages/               # Application pages
│   ├── services/            # API/service logic
│   └── ...
│
├── server/                  # Node.js + Express backend
│   ├── controllers/         # Request handling
│   ├── routes/              # REST API routes
│   ├── models/              # MongoDB models
│   ├── services/            # AI/business logic
│   └── ...
│
├── README.md
└── ...
```

> Update the folder names above if your actual repository uses a
> different structure.

## Getting Started

### Prerequisites

Make sure you have the following installed:

-   [Node.js](https://nodejs.org/)
-   npm
-   MongoDB
-   Git

You will also need an OpenRouter API key.

### 1. Clone the Repository

``` bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <YOUR_PROJECT_DIRECTORY>
```

### 2. Install Dependencies

If the project has separate frontend and backend applications:

``` bash
cd client
npm install

cd ../server
npm install
```

### 3. Configure Environment Variables

Create a `.env` file inside the backend directory.

Example:

``` env
PORT=5000
MONGODB_URI=your_mongodb_connection_string
OPENROUTER_API_KEY=your_openrouter_api_key
JWT_SECRET=your_jwt_secret
CLIENT_URL=http://localhost:5173
```

If your project uses different environment variable names, replace the
examples with the variables used in your implementation.

**Never commit your `.env` file or API keys to GitHub.**

### 4. Start the Backend

``` bash
cd server
npm run dev
```

### 5. Start the Frontend

Open another terminal:

``` bash
cd client
npm run dev
```

The application should now be available at the local development URL
shown by Vite.

## AI Generation Workflow

The core workflow is designed around iterative AI-assisted development:

1.  The user enters a natural-language description of the website.
2.  The frontend sends the request to the backend.
3.  The backend communicates with the selected OpenRouter model.
4.  The AI generates the website structure and React source code.
5.  The application displays generation progress to the user.
6.  The generated project is stored and made available in the workspace.
7.  The user can provide additional prompts to modify the website.
8.  The user can manually edit the generated source code.
9.  The completed website can be exported or published.

## Example Prompt

``` text
Create a modern landing page for a fitness application.

Requirements:
- Hero section with a strong call-to-action
- Features section
- Pricing section
- Testimonials
- Responsive design
- Modern typography
- Clean navigation
```

The AI uses the prompt as the starting point for generating the React
application.

## API Overview

The backend exposes REST APIs for the application's core functionality.

Typical API areas include:

  Area             Purpose
  ---------------- -----------------------------------------------
  Authentication   User signup, login, and session management
  Projects         Create, retrieve, update, and manage projects
  AI Generation    Generate and modify website code
  Code             Store and update generated source code
  Export           Prepare projects for export or publishing

> Update this section with the exact endpoints from your implementation
> before publishing the repository.

## Code Quality

[CodeRabbit](https://www.coderabbit.ai/) is integrated into the
development workflow to provide AI-powered code reviews.

It helps with:

-   Identifying potential bugs
-   Detecting code-quality issues
-   Suggesting improvements
-   Reviewing pull requests
-   Improving maintainability
-   Encouraging production-ready coding practices

## Security Considerations

-   Store secrets in environment variables.
-   Never expose API keys in frontend code.
-   Validate and sanitize user input on the backend.
-   Protect authenticated API routes.
-   Use appropriate database access controls.
-   Avoid committing `.env` files to version control.

## Future Enhancements

Potential improvements for future versions include:

-   Multiple AI model selection
-   Website preview in an isolated sandbox
-   Version history and rollback
-   Collaborative editing
-   One-click deployment to hosting platforms
-   Custom domain support
-   AI-powered debugging
-   Image and asset generation
-   More advanced project templates
-   Usage analytics and subscription plans

## Learning Outcomes

This project provides hands-on experience with:

-   Full-stack MERN application development
-   AI API integration using OpenRouter
-   AI-assisted code generation
-   Prompt engineering
-   REST API development
-   Authentication and authorization
-   MongoDB data modeling
-   React application architecture
-   Code editor integration
-   Export and publishing workflows
-   Production-oriented project organization
-   AI-assisted software development with CodeRabbit

## Contributing

Contributions are welcome.

1.  Fork the repository.
2.  Create a feature branch.

``` bash
git checkout -b feature/your-feature
```

3.  Commit your changes.

``` bash
git commit -m "Add your feature"
```

4.  Push the branch.

``` bash
git push origin feature/your-feature
```

5.  Open a Pull Request.

## License

This project is intended for educational and portfolio purposes. Add
your preferred license here if you plan to distribute the project
publicly.

## Author

**Adiba Khan**

-   GitHub: [@Adibakhan14](https://github.com/Adibakhan14)
-   Portfolio:
    [adibakhan-portfolio.framer.website](https://adibakhan-portfolio.framer.website)

------------------------------------------------------------------------

⭐ If you find this project useful, consider giving the repository a
star.
