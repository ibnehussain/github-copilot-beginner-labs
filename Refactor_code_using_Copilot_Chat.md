# 🔹 LAB: Refactor a Block of Code Using GitHub Copilot Chat

## 🎯 Objective
Learn how to use **GitHub Copilot Chat** to refactor existing code, improve readability, and enhance maintainability.

---

## 🧰 Prerequisites
Ensure the following are set up before starting the lab:

- ✅ Visual Studio Code installed
- ✅ GitHub account with Copilot enabled
- ✅ GitHub Copilot Chat extension installed
- ✅ Basic knowledge of the programming language used (JavaScript in this lab)

---

## 🛠️ Lab Steps

### 1. Setup the Project

1. Create a new folder for the lab:

   ```bash
   mkdir copilot-refactor-lab
   cd copilot-refactor-lab
   ```

2. Open the folder in VS Code.

3. Create a file named `app.js` and paste the following code:

   ```javascript
   function calculate(a, b, c) {
       let result = 0;
       if (a > 0) {
           result += a * 2;
       } else {
           result -= a;
       }
       if (b > 0) {
           result += b * 3;
       } else {
           result -= b;
       }
       if (c > 0) {
           result += c * 4;
       } else {
           result -= c;
       }
       return result;
   }

   console.log(calculate(1, -2, 3));
   ```

> **Note:** This code works but is repetitive and can be refactored.

---

### 2. Open GitHub Copilot Chat

1. Open the **Copilot Chat** panel in VS Code (`Cmd+Shift+P` / `Ctrl+Shift+P` → type `Copilot Chat: Open`).
2. Place your cursor anywhere inside `app.js`.

---

### 3. Ask Copilot to Refactor

1. In the chat input, type:

   ```
   Refactor this function to reduce repetition and make it cleaner.
   ```
2. Review the suggestions provided by Copilot Chat.

---

### 4. Apply the Refactored Code

1. Accept the suggested refactor. For example, Copilot may suggest:

   ```javascript
   function calculate(a, b, c) {
       const values = [a, b, c];
       const multipliers = [2, 3, 4];
       return values.reduce((result, value, index) => {
           return result + (value > 0 ? value * multipliers[index] : -value);
       }, 0);
   }

   console.log(calculate(1, -2, 3));
   ```

2. Save the file (`Ctrl+S` / `Cmd+S`).

---

### 5. Test the Refactored Code

1. Run the code:

   ```bash
   node app.js
   ```
2. Verify the output is the same as before the refactor.

---

### 6. Optional Enhancements

- Ask Copilot to **add comments** to explain the code:

  ```
  Add comments to explain what this function does.
  ```
- Ask Copilot to **rename variables** to make them more descriptive:

  ```
  Suggest better variable names for readability.
  ```

---

### 7. Lab Completion

By completing this lab, you have:

- ✅ Used GitHub Copilot Chat to refactor repetitive code
- ✅ Maintained the same functionality
- ✅ Enhanced code readability using AI assistance

---


