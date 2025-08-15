Angry Compiler 

Welcome to the Angry Compiler\! This is a web-based C language compiler that not only compiles and runs your code but also provides hilariously sarcastic and angry error messages when things go wrong, thanks to the power of a generative AI model.

The project consists of a React frontend and a Node.js backend. The frontend provides an interactive code editor where you can write your C code. When you hit "Compile & Run," the code is sent to the backend, compiled with GCC, and the output or the special "angry" error is returned for you to see.

Features

  - Interactive Code Editor: Write your C code in a clean, syntax-highlighted editor powered by CodeMirror.
  - Compile & Run: Easily compile and execute your C code with a single click.
  - Sarcastic Error Messages: Instead of dry, technical compiler errors, get a witty and "angry" response from an AI that's tired of your mistakes.
    Light/Dark Mode: A simple toggle to switch between light and dark themes for a comfortable coding experience.

Tech Stack

Frontend

  - React
  - CodeMirror
  - Axios
  - CSS Modules (App.css, index.css)

Backend

  - Node.js (Express)
  - Generative AI (Gemini)

Prerequisites

To get this project up and running locally, you'll need the following installed:

  - Node.js (`>=14.0.0`)
  - npm (`>=6`)
  - GCC compiler on your system to handle C code compilation on the backend.

Installation

1.  Clone the repository and navigate to the project directory.

2.  Install the backend dependencies:

    ```sh
    npm install
    ```

3.  Navigate into the client directory (`my_folder`) to install the frontend dependencies:

    ```sh
    cd my_folder
    npm install
    ```

Running the Application

1.  Create a `.env` file in your root directory with your Google Generative AI API key:

    ```
    GEMINI_API_KEY=your_api_key_here
    ```

2.  Start the backend server from the root directory:

    ```sh
    node my_folder/server.js
    ```

    The server will start on `http://localhost:5000`.

3.  In a separate terminal, start the React development server from the `my_folder` directory:

    ```sh
    cd my_folder
    npm start
    ```

    This will run the app in development mode and open `http://localhost:3000` in your browser.

Available Scripts (Frontend)

In the `my_folder` directory, you can run:

  - `npm start`: Runs the app in development mode.
  - `npm test`: Launches the test runner in interactive watch mode.
  - `npm run build`: Builds the app for production to the `build` folder.
  - `npm run eject`: A one-way operation to remove the single build dependency from your project.

Project Structure

  - `my_folder/`: Contains the React frontend and Node.js backend logic.
  - `my_folder/app.js`: The main Express server file for the backend.
  - `my_folder/compileController.js`: Handles the core logic of compiling the C code, executing it, and sending the output or an AI-generated error.
  - `my_folder/compileRoutes.js`: Defines the API routes for the compiler.
  - `my_folder/service/aiService.js`: Contains the logic for connecting to the Gemini AI model to generate "angry" error messages.
  - `my_folder/App.js`: The main React component for the user interface, including the code editor and compile button.
  - `my_folder/header.js`: A React component for the app's header and dark mode toggle.
  - `my_folder/package.json`: Manages the project dependencies and scripts for both the frontend and backend.
