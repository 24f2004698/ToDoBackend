# Node.js template

This is a Node.js project with an HTTP server.

Add your [configuration](https://codesandbox.io/docs/projects/learn/setting-up/tasks) to optimize it for [CodeSandbox](https://codesandbox.io).

## How does this work?

We run `yarn start` to start an HTTP server that runs on http://localhost:8080. You can open new or existing devtools with the + button next to the devtool tabs.

## Resources

- [CodeSandbox — Docs](https://codesandbox.io/docs)
- [CodeSandbox — Discord](https://discord.gg/Ggarp3pX5H)



**ToDo Backend**

A RESTful API service for managing to-do tasks. Built with Node.js and Express, this backend connects to a database to store, retrieve, update, and delete task records.

---

## Features

* **CRUD** operations for to-do tasks via REST endpoints
* Task schema with title, description, completion status, and timestamps
* Data validation and error handling
* CORS enabled for cross-origin access
* Environment-based configuration (development, production)

---

## Tech Stack

* **Node.js** for server runtime
* **Express** for building the API
* **MongoDB** (via Mongoose) or replace with your preferred database
* **dotenv** for environment variable management
* **Joi** or **express-validator** for request validation (optional)

---

## Getting Started

Follow these steps to get the backend running locally.

### Prerequisites

* Node.js (v14 or later)
* npm or yarn package manager
* MongoDB instance (local or Atlas) or your chosen database

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/24f2004698/ToDoBackend.git
   cd ToDoBackend
   ```
2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   ```

### Configuration

1. Create a `.env` file in the project root.
2. Add the following variables (adjust according to your setup):

   ```bash
   PORT=5000
   DB_URI=mongodb://localhost:27017/todo_db
   ```

### Running the Server

```bash
npm start
# or
yarn start
```

By default, the server listens on the port specified in `.env` (e.g., `http://localhost:5000`).

---

## API Endpoints

| Method | Endpoint         | Description                  |
| ------ | ---------------- | ---------------------------- |
| GET    | `/api/tasks`     | Retrieve all tasks           |
| GET    | `/api/tasks/:id` | Retrieve a single task by ID |
| POST   | `/api/tasks`     | Create a new task            |
| PUT    | `/api/tasks/:id` | Update an existing task      |
| DELETE | `/api/tasks/:id` | Delete a task by ID          |

---

## Project Structure

```
ToDoBackend/
├── controllers/    # Request handler functions
├── models/         # Mongoose schemas or ORM models
├── routes/         # Express route definitions
├── middleware/     # Custom middleware (error handling, validation)
├── config/         # Database and environment setup
├── app.js          # Express app configuration
├── server.js       # Entry point to start the server
├── .env            # Environment variables
└── package.json    # Project metadata and scripts
```

---

## Available Scripts

* `npm start` or `yarn start`: Runs the server in production mode
* `npm run dev` or `yarn dev`: Runs the server with nodemon for development
* `npm test` or `yarn test`: Runs test suite (if configured)

---

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m 'Add some feature'`)
4. Push to the branch (`git push origin feature/YourFeature`)
5. Open a pull request

Please adhere to code style conventions and include tests for new functionality.
