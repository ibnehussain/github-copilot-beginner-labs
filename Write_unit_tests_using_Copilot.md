# 🔹 LAB: Write Unit Tests for an Existing Module Using GitHub Copilot

## 🎯 Objective
Learn how to use **GitHub Copilot** to generate unit tests for an existing JavaScript module, ensuring code reliability and correctness.

---

## 🧰 Prerequisites
Ensure the following are set up before starting the lab:

- ✅ Visual Studio Code installed
- ✅ GitHub account with Copilot enabled
- ✅ Node.js installed (v18+ recommended)
- ✅ Basic knowledge of JavaScript and unit testing frameworks (e.g., Jest)

---

## 🛠️ Lab Steps

### 1. Setup the Project

1. Create a new folder for the lab:

   ```bash
   mkdir copilot-unit-test-lab
   ```

2. Navigate to the folder:

   ```bash
   cd copilot-unit-test-lab
   ```

3. Initialize a new Node.js project:

   ```bash
   npm init -y
   ```

4. Install Jest as the testing framework:

   ```bash
   npm install --save-dev jest
   ```

5. Open the folder in VS Code.

---

### 2. Create the Module to Test

1. Create a file named `math.js` and add the following code:

   ```javascript
   function add(a, b) {
       return a + b;
   }

   function subtract(a, b) {
       return a - b;
   }

   module.exports = { add, subtract };
   ```

2. Save the file (`Ctrl+S` / `Cmd+S`).

---

### 3. Generate Unit Tests Using Copilot

1. Create a new file named `math.test.js`.
2. Open the file and type the following comment:

   ```javascript
   // Write unit tests for the add and subtract functions in math.js using Jest
   ```

3. Press **Enter** and accept the Copilot suggestions for the test cases. For example, Copilot may generate:

   ```javascript
   const { add, subtract } = require('./math');

   test('adds two numbers', () => {
       expect(add(2, 3)).toBe(5);
       expect(add(-1, 1)).toBe(0);
   });

   test('subtracts two numbers', () => {
       expect(subtract(5, 3)).toBe(2);
       expect(subtract(0, 5)).toBe(-5);
   });
   ```

4. Save the file.

---

### 4. Run the Tests

1. Add the following script to your `package.json` file under the `scripts` section:

   ```json
   "scripts": {
       "test": "jest"
   }
   ```

2. Run the tests:

   ```bash
   npm test
   ```

3. Verify that all tests pass successfully.

---

### 5. Optional Enhancements

- Add more test cases to cover edge scenarios.
- Ask Copilot to generate tests for additional functions if you expand the `math.js` module.

---

### 6. Lab Completion

By completing this lab, you have:

- ✅ Used GitHub Copilot to generate unit tests for an existing module
- ✅ Verified the correctness of the module using Jest
- ✅ Learned how to enhance test coverage with AI assistance

---