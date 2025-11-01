# NestJS CRUD REST API

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="120" alt="Nest Logo" /></a>
</p>

<p align="center">
  A professional RESTful API built with <a href="http://nestjs.com/" target="_blank">NestJS</a> framework, featuring authentication, user management, and bookmark functionality.
</p>

<p align="center">
  <a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/v/@nestjs/core.svg" alt="NPM Version" /></a>
  <a href="https://www.npmjs.com/~nestjscore" target="_blank"><img src="https://img.shields.io/npm/l/@nestjs/core.svg" alt="Package License" /></a>
  <a href="https://nodejs.org" target="_blank"><img src="https://img.shields.io/node/v/@nestjs/core" alt="Node.js Version" /></a>
</p>

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Project Structure](#-project-structure)
- [Configuration](#-configuration)
- [Running the Application](#-running-the-application)
- [Docker Setup](#-docker-setup)
- [Testing](#-testing)
- [API Documentation](#-api-documentation)
- [Scripts](#-scripts)
- [Development](#-development)

## ✨ Features

- **Authentication Module**: Secure user authentication and authorization
- **User Management**: Complete CRUD operations for user entities
- **Bookmark Management**: Create, read, update, and delete bookmarks
- **RESTful API**: Clean and standardized REST endpoints
- **TypeScript**: Full type safety and enhanced developer experience
- **Docker Support**: Containerized development and testing environments
- **Database**: PostgreSQL with separate databases for development and testing
- **Testing**: Unit and E2E tests with Jest
- **Code Quality**: ESLint and Prettier for consistent code style

## 🛠 Tech Stack

- **Framework**: [NestJS](https://nestjs.com/) v11.0.1
- **Language**: TypeScript 5.7.3
- **Runtime**: Node.js
- **Database**: PostgreSQL 13
- **Containerization**: Docker & Docker Compose
- **Testing**: Jest, Supertest
- **Code Quality**: ESLint, Prettier
- **Package Manager**: Yarn

## 📦 Prerequisites

Before you begin, ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [Yarn](https://yarnpkg.com/) package manager
- [Docker](https://www.docker.com/) and Docker Compose (for database setup)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd nestjs-11-crud-rest-api
   ```

2. **Install dependencies**
   ```bash
   yarn install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

## 📁 Project Structure

```
nestjs-11-crud-rest-api/
├── src/
│   ├── auth/              # Authentication module
│   │   ├── auth.controller.ts
│   │   ├── auth.module.ts
│   │   └── auth.services.ts
│   ├── user/               # User management module
│   │   └── user.module.ts
│   ├── bookmark/           # Bookmark management module
│   │   └── bookmark.module.ts
│   ├── app.module.ts       # Root application module
│   └── main.ts             # Application entry point
├── test/                   # E2E tests
├── docker-compose.yml      # Docker configuration
├── package.json
└── README.md
```

## ⚙️ Configuration

The application uses environment variables for configuration. Key settings include:

- `PORT`: Server port (default: 3333)
- Database connection settings (configured via Docker Compose)

## 🏃 Running the Application

### Development Mode

```bash
# Start the development server with hot-reload
yarn start:dev
```

The application will be available at `http://localhost:3333`

### Production Mode

```bash
# Build the application
yarn build

# Run the production build
yarn start:prod
```

### Debug Mode

```bash
# Start with debugging enabled
yarn start:debug
```

## 🐳 Docker Setup

This project includes Docker Compose configuration for easy database setup.

### Start Database Services

```bash
# Start PostgreSQL databases (development and test)
docker-compose up -d
```

This will start two PostgreSQL instances:
- **Development database**: Available on port `5434`
- **Test database**: Available on port `5435`

### Database Configuration

Both databases are pre-configured with:
- **Username**: `postgres`
- **Password**: `123`
- **Database**: `nest`

### Stop Database Services

```bash
# Stop and remove containers
docker-compose down
```

## 🧪 Testing

### Run Unit Tests

```bash
# Run all unit tests
yarn test

# Run tests in watch mode
yarn test:watch

# Run tests with coverage
yarn test:cov
```

### Run E2E Tests

```bash
# Run end-to-end tests
yarn test:e2e
```

### Debug Tests

```bash
# Run tests with debugging
yarn test:debug
```

## 📚 API Documentation

### Modules

#### Authentication (`/auth`)
Handles user authentication and authorization.

#### Users (`/users`)
Manages user entities and operations.

#### Bookmarks (`/bookmarks`)
Manages bookmark entities and operations.

> **Note**: Full API documentation will be available once the endpoints are implemented.

## 📜 Scripts

| Script | Description |
|--------|-------------|
| `yarn build` | Compile TypeScript to JavaScript |
| `yarn start` | Start the application |
| `yarn start:dev` | Start in development mode with hot-reload |
| `yarn start:debug` | Start in debug mode |
| `yarn start:prod` | Start in production mode |
| `yarn test` | Run unit tests |
| `yarn test:watch` | Run tests in watch mode |
| `yarn test:cov` | Run tests with coverage |
| `yarn test:e2e` | Run end-to-end tests |
| `yarn lint` | Lint and fix code issues |
| `yarn format` | Format code with Prettier |

## 💻 Development

### Code Style

This project uses ESLint and Prettier for code formatting and linting:

```bash
# Lint and fix issues
yarn lint

# Format code
yarn format
```

### Adding New Modules

To add a new module to the application:

1. Generate a new module using NestJS CLI:
   ```bash
   nest generate module <module-name>
   ```

2. Import the module in `app.module.ts`

### Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
PORT=3333
DATABASE_URL=postgresql://postgres:123@localhost:5434/nest
TEST_DATABASE_URL=postgresql://postgres:123@localhost:5435/nest
```

## 📝 License

This project is [UNLICENSED](LICENSE).

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Support

For support, please open an issue in the repository.

---

<p align="center">
  Built with ❤️ using <a href="https://nestjs.com/" target="_blank">NestJS</a>
</p>
