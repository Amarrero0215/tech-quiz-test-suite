# 📊 Tech Quiz Test Suite — Challenge 19

A MERN-based interactive quiz application with **Cypress-driven component and end-to-end testing** to ensure reliability, stability, and user experience under various conditions.

This project simulates a timed tech quiz with randomized questions fetched from a backend API. Users can test their knowledge, view their score, and restart the quiz for continuous improvement.

---

## ✅ Walkthrough Video

🎥 [Click here to watch the full walkthrough video](./Assets/videos/SmallCypressTestWalkthroughFile.mp4)

The video demonstrates:

- Launching the app from the command line
- The quiz UI functioning as expected
- All **Cypress component** and **end-to-end** tests running and **passing**
- Proper mocking of test data using fixtures

---

## 🛠️ Technologies Used

- **React** (frontend)
- **Node.js & Express** (backend)
- **MongoDB with Mongoose** (database)
- **Cypress** (testing)
- **TypeScript** and **Vite** (dev environment)
- **Bootstrap** for styling

---

## 📂 File Structure Overview

```
Develop/
├── client/                 # React frontend
├── server/                 # Express backend + MongoDB connection
├── cypress/                # Cypress testing setup
│   ├── component/          # Component test: Quiz.cy.jsx
│   ├── e2e/                # End-to-end test: quiz.cy.js
│   ├── fixtures/           # Mock quiz data: questions.json
│   └── support/            # Component mount config
├── cypress.config.ts       # Cypress config (component + e2e)
├── .env                    # MongoDB URI (required to run backend)
├── package.json            # Scripts + dependencies
README.md                   # You are here
```

---

## 🚀 How to Run the App Locally

> You'll need Node.js, npm, and MongoDB or MongoDB Atlas setup.

### 1. Clone the repo

```bash
git clone https://github.com/Amarrero0215/tech-quiz-test-suite.git
cd tech-quiz-test-suite
```

### 2. Install dependencies

```bash
cd server && npm install
cd ../client && npm install
cd ..
```

### 3. Configure environment

Create a `.env` file in the `/server` folder:

```env
MONGODB_URI=mongodb+srv://<db_username>:<db_password>@quiz-db.mtbyojw.mongodb.net/<db_nickname>?retryWrites=true&w=majority&appName=QUIZ-db
```

### 4. Seed the database

```bash
cd server
node --loader ts-node/esm src/seeds/seed.ts
```

### 5. Build & Run the backend and frontend

```bash
# In one terminal
cd server
npm run build
npm start

# In another terminal
cd client
npm run build
npm run dev
```

Frontend runs on `http://localhost:3001`.

---

## 🧪 Running Cypress Tests

### 1. Start Cypress GUI

From the root (`Develop/`):

```bash
npm run test
```

### 2. Run both testing suites:

- **Component Testing** → `Quiz.cy.jsx`
- **End-to-End Testing** → `quiz.cy.js`

> Make sure both the frontend and backend servers are running during tests.

---

## 📌 Acceptance Criteria

- ✅ Quiz starts and displays a question
- ✅ Each question is answerable and moves to the next
- ✅ Score is shown at the end
- ✅ Users can restart the quiz
- ✅ Full test coverage using Cypress (component + e2e)
- ✅ Tests use mock data via `cypress/fixtures/questions.json`

---

## 📊 Grading Highlights

- ✅ All tests passing from the Cypress Test Runner
- ✅ Test data properly mocked using fixtures
- ✅ Clean file structure with readable, maintainable code
- ✅ Walkthrough video clearly demonstrating both test suites and command line execution

---

## 💬 Author

**Alex**  
[GitHub](https://github.com/Amarrero0215)

---

© 2024 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.

