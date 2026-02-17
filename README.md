# Quiz CLI

## Project Overview

The **Quiz CLI** is an interactive command-line quiz game aimed at helping users enhance their knowledge in JavaScript, Node.js, and general programming concepts. It demonstrates various modern JavaScript features and techniques such as ES Modules, Promises, and user input handling in a terminal environment. It is educational, fun, and built entirely in Node.js.

Key components of the project include:
- Dynamic loading of quiz questions from a JSON file.
- Terminal-based interaction using readline APIs.
- Modular and reusable code for input handling, quiz logic, and UI styling.

---

## Key Features

- Multi-category quiz game:
  - JavaScript Basics
  - Node.js Fundamentals
  - General Programming
- Selective question counts (e.g., select 3, 5, or all questions).
- Randomized question order.
- Visual progress bar and real-time feedback.
- Explanations for correct and incorrect answers.
- User-friendly and colorful terminal UI via styled text.
- Error handling for a smooth user experience.

---

## Tech Stack & Tools

| Category           | Technology / Tool                          |
|--------------------|-------------------------------------------|
| **Language**       | JavaScript (ES6+)                        |
| **Environment**    | Node.js                                  |
| **Standardization**| ES Modules                               |
| **File Operations**| Node.js `fs/promises` API                |
| **Input Handling** | Node.js `readline` API                   |
| **Terminal Styling**| ANSI Escape Codes via custom library    |

Minimum Node.js version required: `18.0.0`.

---

## Project Structure

Below is an overview of the project directory structure:

```
.
├── index.js         # Main entry point of the application
├── package.json     # Project configuration & dependencies
├── data/
│   └── questions.json # Quiz question bank categorized by topics
├── src/
    ├── colors.js    # Terminal color utilities
    ├── input.js     # Input handling utilities
    ├── quiz.js      # Core quiz game logic
└── .idea/           # (IDE Metadata)
```

### Explanation of Main Modules

- **index.js**: Entrypoint file orchestrating the entire flow of the application. Handles loading questions, setting up input interfaces, running the quiz, and controlling the application loop.
- **data/questions.json**: A JSON file containing the quiz questions organized into categories such as JavaScript Basics, Node.js Fundamentals, etc.
- **src/colors.js**: Defines functions and constants to add colored and styled text to terminal output.
- **src/input.js**: Handles user input using Node.js `readline` module, providing reusable functions for selections, prompts, confirmations, and pauses.
- **src/quiz.js**: Contains the `Quiz` class with core logic for managing questions, checking answers, tracking progress, and providing results.

---

## Prerequisites

Before running the application, ensure you have the following installed on your system:

- **Node.js** (minimum version: `18.0.0`)

---

## Setup & Installation

Follow these steps to set up and run the Quiz CLI locally:

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

No external dependencies are required as the project is built using only Node.js core modules.

---

## Running the Application

### Development Mode

To start the quiz game, run:
```bash
npm start
```

This will:
- Load the quiz question bank.
- Launch a user-friendly command-line interface to play the quiz.

---

## Usage Examples

- Choose a category (e.g., "JavaScript Basics").
- Select the number of questions to attempt (e.g., 3, 5, or all).
- Answer multiple-choice questions by entering the corresponding number of your chosen answer.
- Receive feedback for each question along with explanations for correct/incorrect answers.
- View quiz results and get detailed feedback on incorrect answers.

---

## Configuration

### Question Bank

The `data/questions.json` file contains all quiz questions categorized into topics. You can edit or add new categories and questions in the following format:

```json
{
  "categories": {
    "javascript": {
      "name": "JavaScript Basics",
      "questions": [
        {
          "question": "What keyword is used to declare a constant in JavaScript?",
          "options": ["var", "let", "const", "define"],
          "answer": 2,
          "explanation": "The 'const' keyword declares a block-scoped constant that cannot be reassigned."
        }
      ]
    }
  }
}
```

Fields:
- `question`: The text of the question.
- `options`: An array of possible answers.
- `answer`: The correct answer's index (0-based).
- `explanation`: Explanation shown after the answer is provided.

---

## Getting Started Guide

Here are the steps to familiarize yourself with the repository:

1. Run `npm start` to start the application.
2. Explore the code in `src` and `data` directories:
   - Customize or add more colors in `src/colors.js`.
   - Add new questions or categories in `data/questions.json`.
   - View how the Quiz class implements the core game logic in `src/quiz.js`.
3. Experiment with modifying scripts in `package.json`.

A basic workflow:
- Start the quiz.
- Choose a category and respond to the questions.
- Review your results and explanations to understand mistakes.

---

## Common Troubleshooting

- **Node.js incompatible version**
  - Ensure your system is running Node.js version `18.0.0` or above by running:
    ```bash
    node -v
    ```
- **Missing `questions.json` file**
  - Ensure the `data/questions.json` file exists and has the correct structure.
- **Questions not showing properly**
  - Validate the JSON structure using an online JSON validator.

---

This repository is designed as an educational tool to provide a hands-on coding challenge with modern JavaScript and Node.js. Feel free to customize and extend it as required!