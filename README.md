# Welcome to Our WebCV Project

Welcome to the WebCV project! This is a multi-week course where we'll build a modern CV/Portfolio web application.

## Project Stack

- **Vue 3** with TypeScript
- **Vite** for build tooling
- **Tailwind CSS v4** for styling
- **Vue Router** for navigation
- **Gemini AI API** for AI integration
- **Google Firebase** for database and authentication
- **Frontend animation libraries** for enhanced UX

## Getting Started

### Clone the Repository

```bash
git clone <repository-url>
cd webcvCycle2
```

### Install Dependencies

```bash
yarn install
```

## Branch Structure

This repository is organized by weekly sessions. Each week has its own branch with the completed code for that session.

### Available Branches

- `main` - The main branch (project overview)
- `wk1` - Week 1 starter code

### How to Navigate Between Branches

#### To start working on Week 1:

```bash
git checkout wk1
yarn install
yarn dev
```

#### To switch between weeks:

```bash
# View all available branches
git branch -a

# Switch to a specific week
git checkout wk2  # or wk3, wk4, etc.

# Pull the latest changes
git pull origin <branch-name>
```

#### To create your own working branch:

```bash
# Create a new branch from a week's code
git checkout wk1
git checkout -b my-wk1-work

# Now you can make changes without affecting the original week branch
```

## Development

```bash
# Run development server
yarn dev

# Build for production
yarn build

# Preview production build
yarn preview
```

## Course Structure

Throughout this course, you'll learn to:
- Build a responsive Vue 3 application with TypeScript
- Style with Tailwind CSS v4
- Integrate Gemini AI API for intelligent features
- Set up Firebase for backend services
- Add beautiful animations to enhance user experience
- Create a fully functional CV/Portfolio website

Happy coding!
