# Aider_ReactCalculator

🧮 **React Calculator Enhancement Project**  
A fork of the original React Calculator, enhanced using the Aider AI-assisted development tool to add meaningful features like keyboard input support and backspace functionality.

This project demonstrates how Aider can be used effectively for real-world enhancements while following best practices in prompt engineering, Git version control, and iterative development.

---

## 📌 Original Project Functionality

The original React Calculator provides a basic calculator interface that allows users to perform:

- Addition  
- Subtraction  
- Multiplication  
- Division  

**Key Features:**

- Display panel showing current expression and result  
- Button panel with numeric keys and operators  
- Logic for evaluating expressions and updating state  
- Basic styling and layout  
- Users interact with the app via mouse or touch input only  

---

## ✅ Added Features

### 1. Keyboard Input Support

**User Story:**  
_As a user, I want to use my keyboard to input numbers, operators, and actions so I can operate the calculator faster without needing to use the mouse._

**Implementation Summary:**

Aider helped implement logic in `App.js` that listens for key events and maps them to corresponding calculator actions. The feature supports:

- Number keys (0–9)  
- Operators: `+`, `-`, `/` 
- Escape key for clear (`AC`)  
- Decimal point (`.`)  

**Challenges Faced:**

- Initial implementation did not integrate correctly with existing button handlers  
- Some key mappings (like Enter) didn’t trigger calculation until refined  
- Conflicts with browser default behaviors were handled by limiting scope of event listener  

**Solution Approach:**

After reviewing the code with Aider using `/ask`, I requested a refined implementation with more specific instructions. This led to successful integration with minimal changes to existing logic.

---

### 2. Backspace Functionality

**User Story:**  
_As a user, I want to correct input mistakes without clearing everything, improving usability and reducing frustration._

**Implementation Summary:**

- A new `"⌫"` button was added to the UI  
- Functionality implemented in `App.js` to remove the last character of the current expression  
- Supports:
  - Removal of digits one at a time  
  - Safe handling of decimals and negative values  
  - Prevention of empty display by ensuring `0` is shown when needed  

**Challenges Faced:**

- Handling partial expressions required careful manipulation of state  
- Edge cases like removing characters after an operator or decimal point caused unexpected behavior  

**Solution Approach:**

With Aider’s help and iterative refinements, I ensured consistent and safe behavior across all input types.

---

## ⚙️ Implementation Process

1. Forked and cloned the original React Calculator repository locally  
2. Started Aider in the project directory and added relevant files to context using `/add`  
3. Used `/ask` to understand how the app worked before making any changes  
4. Implemented keyboard input support using natural language prompts  
5. Reviewed proposed changes using `/diff` and applied them after confirming correctness  
6. Fixed visual issues (black text on black background) by adjusting styles with Aider  
7. Implemented backspace functionality and refined it through testing  
8. Committed both features using `/commit`  

Each step was documented and tested using `npm start`.

---

## 🔍 Challenges and Solutions

| Challenge                            | Solution                                                                 |
|-------------------------------------|--------------------------------------------------------------------------|
| Keyboard input not working reliably | Refactored event listener and synced with button logic                   |
| Backspace breaking expressions      | Added validation to avoid invalid expressions                            |
| History panel unreadable            | Prompted Aider to fix styles for better contrast                         |
| Git confusion during branching      | Used feature branches and separate commits per feature                   |

---

## 🧠 Aider Commands Used and Their Effectiveness

- `/add` – Added core files (e.g., `App.js`, `calculate.js`) to context  
- `/ask` – Understood unfamiliar code  
- `/implement` – Requested full feature implementations  
- `/diff` – Reviewed proposed changes before applying  
- `/edit` – Made direct edits to refine implementations  
- `/test` – Simulated manual testing via dev server  
- `/run` – Ran `npm start` for live testing  
- `/commit` – Tracked and documented progress  

These commands helped implement complex features with minimal trial and error.

---

## 🚀 How to Run the App

1. **Clone the repo:**

```bash
git clone https://github.com/your-username/react_calculator.git
```
2. **Navigate into the project folder::**

```bash
cd react_calculator
```

3. **Install dependencies:**

```bash
npm install
```

4. **Start the development server:**

```bash
npm start
```

5. Open the app in your browser at http://localhost:3000

Try using the keyboard and backspace functionality to test the enhancements.
