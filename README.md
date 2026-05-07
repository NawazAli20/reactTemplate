# React Template using Parcel build tool

This repo will serve as a starting repo for working with react using parcel build 

# Install dependecies 
After cloning the repo, issue: 

npm install 

# How to run: 

npm start

/****************** Manual setup React Environment ******************************/
# React Environment Setup using Parcel (Manual setup to get your hand dirty)

This guide explains how to create a basic React development environment using **Parcel** as the build tool.

---

# 1. Create a New Project Folder

Open a terminal/console and run:

```bash
mkdir react-project
```

---

# 2. Navigate to the Project Folder

```bash
cd react-project
```

---

# 3. Initialize the Project

Create a default `package.json` file:

```bash
npm init -y
```

---

# 4. Install Parcel

Install Parcel as a development dependency:

```bash
npm install --save-dev parcel
```

Parcel is a build tool that bundles and serves the React application.

---

# 5. Install React and ReactDOM

```bash
npm install react react-dom
```

- `react` → Core React library
- `react-dom` → Renders React components into the browser DOM

---

# 6. Update `package.json`

Open `package.json`.

## Remove the `"main"` line

Remove:

```json
"main": "index.js",
```

---

## Add a `"start"` script

Update the `"scripts"` section:

```json
"scripts": {
  "start": "parcel src/index.html --open -p 8080"
}
```

### Explanation

- `parcel src/index.html`
  - Starts the Parcel development server

- `--open`
  - Automatically opens the browser

- `-p 8080`
  - Runs the application on port `8080`

---

# 7. Create the Project Structure

Create a `src` folder:

```bash
mkdir src
```

Inside `src`, create the following files:

```text
src/
│
├── index.html
├── index.js
└── App.js
```

---

# 8. Example Files

## `src/index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>React App</title>
</head>
<body>
  <div id="root"></div>

  <script type="module" src="./index.js"></script>
</body>
</html>
```

---

## `src/index.js`

```javascript
import React from "react";
import ReactDOM from "react-dom/client";
import App from "./App";

const root = ReactDOM.createRoot(document.getElementById("root"));

root.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>
);
```

---

## `src/App.js`

```javascript
import React from "react";

function App() {
  return (
    <>
      <h1>Welcome to React!</h1>
      <p>Your React environment is working correctly.</p>
    </>
  );
}

export default App;
```

---

# 9. Start the Development Server

Run:

```bash
npm start
```

A browser window should automatically open at:

```text
http://localhost:8080
```

---

# 10. Project Structure Summary

```text
react-project/
│
├── node_modules/
├── package.json
├── package-lock.json
│
└── src/
    ├── index.html
    ├── index.js
    └── App.js
```

---

# 11. Useful Commands

## Start Development Server

```bash
npm start
```

## Install a New Package

```bash
npm install package-name
```

## Remove Parcel Cache (if needed)

```bash
rm -rf .parcel-cache dist
```

---

# 12. Notes

- JSX syntax is automatically compiled by Parcel.
- React components should begin with uppercase letters.
- `React.StrictMode` helps detect development-time issues.
- Parcel automatically reloads the browser when files change.

---

# 13. Recommended Extensions for VS Code
- html-essentials
- HTML CSS Support
- ES7+ React/Redux snippets
- Prettier
- Live Server
- Live Server Preview
- Auto Rename Tag

---

# 14. Next Steps

You can now:
- Create reusable React components
- Add React Router
- Use JSON data files
- Connect APIs
- Deploy to GitHub Pages
- Build portfolio applications

