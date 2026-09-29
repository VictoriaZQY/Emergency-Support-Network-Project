# Emergency-Support-Network Project
This is a course assignment, so the details of implementation can't be publicly shown.

## Readme.md in Original Project
This is the team repo for the ESN application (18652). The layout follows a modern web-app mono-repo structure: use-case folders under `client/` and `server/`, with tests split into unit and integration suites. It does not use a legacy `src/`, `public/`, or `bin/` tree.

```text
|-- client
|   |-- static
|   |   |-- styles
|   |-- home
|   |-- join-community.client
|-- server
|   |-- models
|   |-- controllers
|   |-- routes
|   |-- middleware
|   |-- db
|-- tests
|   |-- unit.tests
|   |-- integ.tests
|-- docs
|-- .env.template
|-- package.json
```

Shared client/server artifacts would go in `common/` when they exist. Config that is not `package.json` or `.gitignore` stays at the repo root (`.env.template`).

## Technology Selection

For Iteration 0, our team researched and discussed technologies for the front-end, back-end, database, and communication between application tiers. We selected a stack that satisfies the course constraints while keeping the project lightweight and manageable for the entire team.

## Selected Technology Stack

### Front-End: HTML5, CSS, Vanilla JavaScript, Bootstrap

We selected HTML5, CSS, and vanilla JavaScript because they satisfy the course requirement to use the standard web stack without front-end frameworks such as React, Vue, Angular, or Ember.

Bootstrap was selected to help us build a responsive interface more quickly. Since the ESN application will be used on devices with different screen sizes, Bootstrap provides useful layout and responsive components without adding a heavy framework.
<img width="1476" height="1488" alt="image" src="https://github.com/user-attachments/assets/699fb9fc-e89c-4159-8a05-a50811cab083" />
<img width="482" height="976" alt="image" src="https://github.com/user-attachments/assets/9f5cb683-3ef0-4080-a2d2-8e75497fff15" />
<img width="1496" height="1500" alt="image" src="https://github.com/user-attachments/assets/de74606b-8f17-4fa5-8512-aebfcf5775d6" />


### Back-End: Node.js and Express.js

We selected Node.js because the project requires server-side JavaScript.

Express.js was selected because it is lightweight and provides a simple way to define routes, middleware, and REST-style API endpoints. It allows us to organize the back-end without introducing unnecessary complexity.

### Database: MongoDB

We selected MongoDB for persistent data storage.

MongoDB works well with Node.js because both applications and database documents can be represented naturally using JavaScript-style objects and JSON. This makes it straightforward to store and retrieve ESN data such as users, communities, statuses, and other application information.

MongoDB also provides flexibility as the structure of the ESN application evolves across later iterations, which can reduce the amount of schema modification needed during development.

### Communication Between Front-End and Back-End: HTTP, REST-style APIs, and JSON

The browser client will communicate with the Express server using HTTP requests.

We selected REST-style APIs because they provide a clear separation between the front-end and back-end tiers and align with the project's future RESTfulness requirements.

JSON will be used as the data exchange format because it is directly supported by JavaScript on both the browser and Node.js sides and works naturally with MongoDB documents.

### Styling Library: Bootstrap

Bootstrap was selected because it provides a simple way to build responsive layouts without introducing a prohibited front-end framework.

It will help us support different screen sizes while keeping our CSS implementation relatively simple.

### Version Control and Project Management: GitHub and GitHub Projects

GitHub will be used for source code management, collaboration, pull requests, and code review.

GitHub Projects will be used as the team's Kanban board for:

- backlog management
- iteration planning
- task assignment
- progress tracking
- Planning Poker estimates
- knowledge-gap action items

### Package Management: npm

npm will be used to manage Node.js dependencies such as Express and MongoDB-related packages.

We selected npm because it is the standard package manager for Node.js and makes it easy for every team member to install the same project dependencies.

## Technology Alternatives Considered

### PostgreSQL vs. MongoDB

We considered both PostgreSQL and MongoDB.

PostgreSQL provides strong relational modeling, but we selected MongoDB because it integrates naturally with Node.js and JSON-based application data and provides more flexibility while our application's data structures are still evolving.

### Plain CSS vs. Bootstrap

We considered using only custom CSS.

We selected Bootstrap because it reduces the amount of responsive layout code we need to write and helps us satisfy the project's mobile responsiveness requirement more quickly.

### Express.js vs. Other Node.js Back-End Frameworks

We considered other Node.js server frameworks, but selected Express.js because it is lightweight, widely used, and provides the functionality we need without adding unnecessary complexity.

## Development Environment Setup

Prerequisites are [Git](https://git-scm.com/downloads), the current LTS version of [Node.js](https://nodejs.org/), and npm (included with Node.js). The team uses a shared [MongoDB Atlas](https://www.mongodb.com/atlas) cluster (see below). Local [MongoDB Community Server](https://www.mongodb.com/try/download/community) is optional for offline work only.

Clone the repository and enter its directory:

```bash
git clone https://github.com/cmu-fse-sa3/f26-esn.git
cd f26-esn
```

Install the project dependencies from the repository root:

```bash
npm install
```

`npm install` reads `package.json` and `package-lock.json` to reproduce the project's dependencies, including Express, Mongoose, bcrypt, JWT and cookie handling, dotenv, and the nodemon development tool. `node_modules/` is excluded from Git.

Copy the template environment file and adjust it for your machine:

```bash
cp .env.template .env
```

Do not commit your local `.env`.

### Shared MongoDB (whole team)

The team uses one Atlas cluster so Join, Login, Directory, and Chat Publicly see the same `citizens` and `publicMessages`. You do **not** need MongoDB installed locally.


## Development Tools

The team will use:

- GitHub for source control, pull requests, and code review.
- GitHub Projects for backlog management, iteration planning, task assignments, estimates, and progress tracking.
- npm for dependency management.
- Visual Studio Code or another suitable editor for development.
- Browser developer tools and terminal tools for debugging.
