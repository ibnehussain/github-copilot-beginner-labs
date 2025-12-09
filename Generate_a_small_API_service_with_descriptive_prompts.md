# 🔹 LAB 1: Generate a Small API Service with Descriptive Prompts

## 🎯 Objective
Participants will learn how to:
- Use **descriptive prompts** to generate a backend API service
- Understand basic **CRUD operations**
- Run and test the generated API locally
- Experience how **prompt quality directly impacts code quality**

---

## 🧰 Prerequisites
Make sure the following are installed:

- ✅ Node.js (v18+)
- ✅ VS Code
- ✅ Postman or Thunder Client (VS Code Extension)
- ✅ Git
- ✅ Internet access (for AI tool usage)

---

## ✅ Step 1: Clone the Repository

Run the following commands to clone the repository and set up the project:

```bash
git clone https://github.com/bezkoder/node-express-mongodb.git
cd nodejs-express-mongodb
npm install
npm start
```

> **Note:** If MongoDB is not connected, proceed to the next steps — we will replace the database with in-memory storage.

---

## ✅ Step 2: Generate In-Memory CRUD Using Copilot

1. Open the file:
   ```
   app/controllers/tutorial.controller.js
   ```

2. Delete all existing content in the file and paste the following comment:

   ```js
   /*
   Generate full in-memory CRUD operations for Tutorial entity.
   Fields:
   - id
   - title
   - description
   - published (boolean)

   Use an array as database.
   Implement:
   - create
   - findAll
   - findOne
   - update
   - delete
   - deleteAll

   Return JSON responses with proper HTTP status codes.
   */
   ```

3. Press **Enter** and accept the Copilot suggestion.

---

## ✅ Step 3: Generate Routes Using Copilot

1. Open the file:
   ```
   app/routes/tutorial.routes.js
   ```

2. Replace the content with the following comment:

   ```js
   /*
   Create Express routes for Tutorial CRUD:
   POST /api/tutorials
   GET /api/tutorials
   GET /api/tutorials/:id
   PUT /api/tutorials/:id
   DELETE /api/tutorials/:id
   DELETE /api/tutorials
   */
   ```

3. Accept the Copilot suggestion.

---

## ✅ Step 4: Add Validation Using Copilot Chat

1. Select the `create` function in the `tutorial.controller.js` file.
2. Ask Copilot Chat:

   > Add request body validation for title and description with proper error messages

---

## ✅ Step 5: Test APIs

Use the following endpoints to test the API:

### Create Tutorial
**Request:**
```
POST http://localhost:8080/api/tutorials
{
  "title": "Copilot Lab",
  "description": "CRUD API using AI",
  "published": true
}
```

### Get All Tutorials
**Request:**
```
GET http://localhost:8080/api/tutorials
```

### Update Tutorial
**Request:**
```
PUT http://localhost:8080/api/tutorials/1
```

### Delete Tutorial
**Request:**
```
DELETE http://localhost:8080/api/tutorials/1
```

---