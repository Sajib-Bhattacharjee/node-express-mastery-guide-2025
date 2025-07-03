<p align="center">
  <img src="images/logo__img.png" alt="node express mastery guide" style="max-width: 100%; height: auto; border-radius: 12px; box-shadow: 0 4px 24px rgba(0,0,0,0.12);">
</p> 



<div align="center"> 

#### 🌟 **Infographic Preview** → [**Node-Express**](https://node-express-infographic.netlify.app/) 💕

🎉 Click to explore the fun and laughter! 😄

</div>


## 📑 Table of Contents

### 🧩 Part 1: Introduction to Node.js

- 1.1 What is Node.js?
  - A Brief History
  - The V8 Engine
  - Event-Driven, Non-Blocking I/O
- 1.2 Setting Up Your Environment
  - Installing Node.js and npm
  - Using Node Version Manager (nvm)
  - Your First "Hello World" Application
- 1.3 The Node.js REPL
- 1.4 Understanding npm (Node Package Manager)
  - package.json and package-lock.json
  - Installing, Updating, and Removing Packages
  - Scripts in package.json

### 📘 Chapter 2: Node.js Core Concepts

- 2.1 The Module System
  - CommonJS (require, module.exports)
  - ES Modules (import, export)
- 2.2 The Event Loop
  - Phases of the Event Loop
  - Understanding Callbacks, Promises, and Async/Await
- 2.3 Buffers, Streams, and Events
  - Working with Binary Data (Buffers)
  - Readable and Writable Streams
  - The EventEmitter Class

### 📘 Chapter 3: Core Node.js Modules

- 3.1 File System (fs module)
  - Reading and Writing Files
  - Working with Directories
  - File Streams
- 3.2 Path (path module)
- 3.3 HTTP (http module)
  - Creating a Simple Web Server
  - Handling Requests and Responses
- 3.4 OS and Process
  - Accessing OS Information
  - Working with the Current Process

### 🚀 Part 2: Building with Express.js

- 4.1 What is Express.js?
  - Why Use a Framework?
- 4.2 Setting Up Your First Express Server
- 4.3 Basic Routing
  - HTTP Methods
  - Route Parameters
  - Query Strings
- 4.4 Handling Requests and Responses
  - request and response Objects
  - Sending JSON, HTML, and Files

### 📘 Chapter 5: Middleware in Express.js

- 5.1 What is Middleware?
- 5.2 Writing Custom Middleware
- 5.3 Using Built-in Middleware
  - express.json()
  - express.urlencoded()
  - express.static()
- 5.4 Third-Party Middleware
- 5.5 Error Handling Middleware

### 📘 Chapter 6: Advanced Routing and Organization

- 6.1 Using the Express Router
- 6.2 Structuring Your Application
- 6.3 Route Groups and Prefixes

### 🛢️ Part 3: Data and Databases

- 7.1 Introduction to Databases
- 7.2 MongoDB with Mongoose
  - Schemas, Models, CRUD
- 7.3 SQL with Sequelize
  - Models, Migrations, CRUD

### 📘 Chapter 8: Template Engines

- 8.1 What are Template Engines?
- 8.2 Using EJS
- 8.3 Using Pug
- 8.4 Using Handlebars

### 🌐 Part 4: Building a REST API

- 9.1 Principles of REST
- 9.2 API Versioning
- 9.3 Status Codes & Error Handling

### 📘 Chapter 10: Authentication and Authorization

- 10.1 Basic Authentication
- 10.2 Session-Based (express-session)
- 10.3 Token-Based (JWT)
- 10.4 OAuth & Social Logins

### 📘 Chapter 11: Security Best Practices

- 11.1 Common Vulnerabilities
- 11.2 Helmet.js
- 11.3 Environment Variables (dotenv)

### ⚙️ Part 5: Advanced Topics and Deployment

- 12.1 Introduction to WebSockets
- 12.2 Using Socket.IO

### 📘 Chapter 13: Testing Your Application

- 13.1 Unit Testing
- 13.2 Integration Testing
- 13.3 End-to-End Testing

### 📘 Chapter 14: Performance and Scalability

- 14.1 Caching Strategies
- 14.2 Cluster Module
- 14.3 PM2 Process Manager

### 📘 Chapter 15: Deployment

- 15.1 Preparing for Production
- 15.2 Deploying to Heroku
- 15.3 Deploying to VPS (Nginx)
- 15.4 Docker Containerization

### 📎 Appendix

- A. Useful npm Packages
- B. Cheat Sheet
- C. Debugging Techniques

---

# 🔥 Getting Started with Node.js

This chapter gets you started with Node.js. You'll learn what it is, how to install it, and how to write your first program.

---

## 🚀 1.1. What is Node.js?

Simply put, **Node.js** is a tool that lets you run JavaScript code on your computer's server, instead of just in a web browser. This means you can use JavaScript to build the entire backend of a web application, from handling web requests to working with databases.

### A Brief History:

Created by Ryan Dahl in 2009, Node.js was designed to solve a common problem: web servers getting stuck while handling many user requests at once. Its unique approach allows it to handle thousands of simultaneous connections efficiently.

### The V8 Engine:

Node.js is built on Google's **V8 JavaScript engine**, the same high-performance engine that powers the Chrome browser. V8 compiles your JavaScript into machine code that the computer can execute very quickly.

### Event-Driven, Non-Blocking I/O:

This is the core magic of Node.js. Instead of handling one request and waiting for it to finish before starting the next (**blocking**), Node.js uses an "**event loop**". It takes a request, starts the task (like reading a file), and immediately moves to the next request without waiting. When the first task is done, it sends a notification (an **event**), and Node.js processes the result. This non-blocking model makes it incredibly efficient for applications that involve a lot of I/O operations, like chat apps or data-streaming services.

---

## 🛠️ 1.2. Setting Up Your Environment

Let's get your computer ready for Node.js development.

### Installing Node.js and npm:

The easiest way to install Node.js is to download the **LTS (Long-Term Support)** version from the official [nodejs.org](https://nodejs.org) website. The LTS version is the most stable. Installing Node.js also automatically installs **npm (Node Package Manager)**, a crucial tool for managing the external libraries (packages) your project will use.

To check if the installation worked, open your terminal or command prompt and run:

```bash
node -v
npm -v
```

✅ If you see version numbers displayed, you're all set!

### Using Node Version Manager (nvm):

Different projects might require different versions of Node.js. **nvm** is a tool that lets you easily install and switch between multiple Node.js versions on your machine. This is particularly useful for developers working on multiple projects with varying Node.js dependencies.

### Your First "Hello World" Application:

1. Create a file named `app.js`.
2. Add this single line of code:

   ```javascript
   console.log("Hello World");
   ```

3. In your terminal, navigate to the file's directory and run:

   ```bash
   node app.js
   ```

   You'll see "Hello World" printed on your screen. Congratulations! 🎉

---

## 💡 1.3. The Node.js REPL

**REPL** stands for **Read-Eval-Print Loop**. It's an interactive console where you can type and test JavaScript code snippets on the fly without creating a file.

Just type `node` in your terminal to start it:

```bash
node
```

```
> console.log("This is a test.");
This is a test.
undefined
> 1 + 1
2
>
```

It's a great playground for quick experiments and debugging!

---

## 📦 1.4. Understanding npm (Node Package Manager)

**npm** is the world's largest software library. It's a command-line tool and an online registry of open-source packages that you can add to your project. Think of it as a massive collection of pre-written code that you can easily integrate into your applications.

### `package.json` and `package-lock.json`:

- **`package.json`**: This is the heart of your project. It lists project metadata (like its name and version) and, most importantly, the packages it depends on. You create it by running `npm init -y` in your project folder.

  ```bash
  npm init -y
  ```

  This command will generate a default `package.json` file, which you can then customize.

- **`package-lock.json`**: This file is automatically generated and records the exact version of every package you've installed, including their dependencies. This ensures that anyone else working on the project gets the exact same setup, preventing "it works on my machine" problems. **Never manually edit this file.**

### Installing, Updating, and Removing Packages:

- **Install**: To add a new package to your project, use `npm install`. This will download the package and add it to your `node_modules` directory and list it as a dependency in `package.json`.

  ```bash
  npm install lodash
  ```

  (installs the "lodash" package, a popular utility library)

- **Update**: To update an installed package to its latest compatible version, use `npm update`.

  ```bash
  npm update lodash
  ```

  (updates it to the latest version)

- **Remove**: To uninstall a package from your project, use `npm uninstall`. This will remove it from `node_modules` and from your `package.json`.

  ```bash
  npm uninstall lodash
  ```

  (removes it from your project)

### Scripts in `package.json`:

You can define command shortcuts in the `scripts` section of `package.json`. This is incredibly useful for automating common tasks like starting your application, running tests, or building your project.

For example, instead of typing `node app.js` every time to run your application, you can add a script:

```json
"scripts": {
  "start": "node app.js",
  "test": "echo \"Error: no test specified\" && exit 1"
}
```

And then simply run:

```bash
npm start
```

This will execute the `node app.js` command. You can define many custom scripts to streamline your development workflow.

# 🔥 Chapter 2: Node.js Core Concepts

Now we'll dive into the fundamental building blocks of any Node.js application.

---

## 📦 2.1. The Module System

To keep code organized and reusable, Node.js uses **modules**. Think of a module as a single, self-contained file of code.

### CommonJS (`require`, `module.exports`):

This is the traditional Node.js way of handling modules. You use `module.exports` to expose functions or variables from a file and `require()` to import them into another file.

#### `math.js`

```javascript
const add = (x, y) => x + y;
module.exports = { add };
```

#### `app.js`

```javascript
const math = require("./math.js");
console.log(math.add(2, 3)); // 5
```

💡 **Key takeaway**: CommonJS is synchronous, meaning modules are loaded one after another.

### ES Modules (`import`, `export`):

This is the modern, standardized JavaScript way. You use `export` to expose code and `import` to bring it in. To use it in Node.js, add `"type": "module"` to your `package.json` file.

#### `package.json`

```json
{
  "name": "my-node-app",
  "version": "1.0.0",
  "type": "module", // Add this line for ES Modules
  "main": "app.mjs",
  "scripts": {
    "start": "node app.mjs"
  }
}
```

#### `math.mjs`

```javascript
export const add = (x, y) => x + y;
```

#### `app.mjs`

```javascript
import { add } from "./math.mjs";
console.log(add(2, 3)); // 5
```

💡 **Key takeaway**: ES Modules are asynchronous, allowing for better optimization and tree-shaking (removing unused code).

---

## 🔄 2.2. The Event Loop

As mentioned, the **event loop** is how Node.js achieves its non-blocking concurrency. It's a loop that constantly checks for and executes completed tasks.

### Phases of the Event Loop:

The loop has specific phases (like timers, I/O polling, and checks) to handle different types of asynchronous operations in an orderly fashion. You don't usually interact with the phases directly, but it's good to know they exist:

1.  **Timers**: Executes `setTimeout()` and `setInterval()` callbacks.
2.  **Pending Callbacks**: Executes I/O callbacks deferred to the next loop iteration.
3.  **Idle, Prepare**: Internal only.
4.  **Poll**: Retrieves new I/O events; executes I/O related callbacks (almost all of them).
5.  **Check**: Executes `setImmediate()` callbacks.
6.  **Close Callbacks**: Executes some close callbacks, e.g., `socket.on('close', ...)`.

### Understanding Callbacks, Promises, and Async/Await:

These are three ways to handle the results of asynchronous operations in Node.js.

#### Callbacks:

A function you pass to another function, which gets called when the operation completes.
❌ **Problem**: Nesting too many callbacks leads to "**callback hell**," which is hard to read and maintain.

```javascript
// Callback example (simplified)
fs.readFile("file.txt", "utf8", (err, data) => {
  if (err) {
    console.error("Error reading file:", err);
    return;
  }
  console.log("File content:", data);

  // Nested callback leading to callback hell
  anotherAsyncFunction(data, (err2, result) => {
    if (err2) return;
    console.log("Another result:", result);
    // ... more nesting
  });
});
```

#### Promises:

An object that represents a future result of an asynchronous operation. It can be in one of three states:

- **Pending**: Initial state, neither fulfilled nor rejected.
- **Fulfilled**: Meaning the operation completed successfully.
- **Rejected**: Meaning the operation failed.

Promises allow you to chain operations with `.then()` and handle errors with `.catch()`, making code cleaner than traditional callbacks.

```javascript
// Promise example
function readFilePromise(filePath) {
  return new Promise((resolve, reject) => {
    fs.readFile(filePath, "utf8", (err, data) => {
      if (err) {
        reject(err);
      } else {
        resolve(data);
      }
    });
  });
}

readFilePromise("file.txt")
  .then((data) => {
    console.log("File content (Promise):", data);
    return anotherPromiseFunction(data);
  })
  .then((result) => {
    console.log("Another result (Promise):", result);
  })
  .catch((error) => {
    console.error("Failed with Promise:", error);
  });
```

#### Async/Await:

This is modern syntactic sugar built on top of Promises.

- The `async` keyword makes a function return a Promise.
- The `await` keyword pauses the execution of an `async` function until a Promise settles (either fulfilled or rejected).

It lets you write asynchronous code that looks clean and linear, as if it were synchronous. It's the **preferred method today** for managing asynchronous operations due to its readability and ease of error handling.

```javascript
// async/await example
async function getUser() {
  try {
    const response = await fetch("https://api.github.com/users/github"); // await pauses execution until fetch completes
    if (!response.ok) {
      // Check for HTTP errors
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    const data = await response.json(); // await pauses until JSON parsing completes
    console.log(data.name);
  } catch (error) {
    console.error("Failed to fetch user:", error);
  }
}

getUser(); // Call the async function
```

✅ **Best Practice**: Always use `try...catch` blocks with `async/await` to handle potential errors gracefully.

---

## 💾 2.3. Buffers, Streams, and Events

These are essential for handling data, especially large amounts of it.

### Working with Binary Data (Buffers):

A **Buffer** is a raw, fixed-size chunk of memory used to handle binary data (like images, audio, or raw network data), which JavaScript isn't traditionally good at. Buffers are instances of the `Buffer` class.

```javascript
const buf = Buffer.from("Hello Node.js!", "utf8");
console.log(buf); // <Buffer 48 65 6c 6c 6f 20 4e 6f 64 65 2e 6a 73 21>
console.log(buf.toString("hex")); // 48656c6c6f204e6f64652e6a7321
```

### Readable and Writable Streams:

Instead of reading a huge file into memory all at once (which could crash your app), you use **streams** to process data piece by piece (in chunks). This makes them incredibly efficient for large data operations.

- A **Readable Stream** lets you read data from a source (like a file, network request, or standard input).
- A **Writable Stream** lets you write data to a destination (like a file, network response, or standard output).

The `.pipe()` method is a beautiful and efficient way to connect a readable stream to a writable stream, for example, to copy a large file or process data without consuming much memory.

```javascript
const fs = require("fs");

// Example: Copying a large file using streams
const readStream = fs.createReadStream("input.txt");
const writeStream = fs.createWriteStream("output.txt");

readStream.pipe(writeStream); // Efficiently pipes data from input.txt to output.txt

readStream.on("end", () => {
  console.log("File copying complete!");
});

readStream.on("error", (err) => {
  console.error("Error during streaming:", err);
});
```

### The EventEmitter Class:

Many objects in Node.js (like streams, HTTP servers, etc.) are "**event emitters**." They can emit named events that you can listen for with `.on()` (or `.addListener()`). This is the core of Node's event-driven architecture.

You can also create your own custom event emitters to build powerful, decoupled systems where different parts of your application communicate by emitting and listening for events.

```javascript
const EventEmitter = require("events");

class MyEmitter extends EventEmitter {}

const myEmitter = new MyEmitter();

myEmitter.on("event", () => {
  console.log("An event occurred!");
});

myEmitter.emit("event"); // Triggers the 'event' listener

myEmitter.on("greet", (name) => {
  console.log(`Hello, ${name}!`);
});

myEmitter.emit("greet", "Alice"); // Emits 'greet' with an argument
```

---

# 📚 Chapter 3: Core Node.js Modules

Node.js comes with a standard library of powerful, built-in modules. You don't need to install them; just `require()` them.

---

## 📁 3.1. File System (`fs` module)

The `fs` module gives you everything you need to work with the file system.

### Reading and Writing Files:

You can read and write files either **asynchronously** (non-blocking, recommended for performance) or **synchronously** (blocking, can freeze your application for long operations).

- **Async Example:** (Preferred for most operations)

  ```javascript
  const fs = require("fs");

  fs.readFile("file.txt", "utf8", (err, data) => {
    if (err) {
      console.error("Error reading file asynchronously:", err);
      return;
    }
    console.log("Async file content:", data);
  });

  fs.writeFile("new_file.txt", "Hello from Node.js!", (err) => {
    if (err) {
      console.error("Error writing file asynchronously:", err);
      return;
    }
    console.log("new_file.txt written successfully (async)!");
  });
  ```

- **Sync Example:** (Use with caution for small, quick operations)

  ```javascript
  try {
    const data = fs.readFileSync("file.txt", "utf8");
    console.log("Sync file content:", data);
    fs.writeFileSync("another_file.txt", "Synchronous write!");
    console.log("another_file.txt written successfully (sync)!");
  } catch (err) {
    console.error("Error during synchronous file operation:", err);
  }
  ```

### Working with Directories:

You can create (`fs.mkdir`), read (`fs.readdir`), and delete directories (`fs.rmdir` or `fs.rm` for recursive deletion).

```javascript
const fs = require("fs");

fs.mkdir("./my_directory", { recursive: true }, (err) => {
  if (err) console.error("Error creating directory:", err);
  else console.log("Directory created or already exists.");
});

fs.readdir(".", (err, files) => {
  // Read current directory
  if (err) console.error("Error reading directory:", err);
  else console.log("Files in current directory:", files);
});
```

### File Streams:

The `fs` module provides methods like `fs.createReadStream()` and `fs.createWriteStream()` to handle files as streams, enabling efficient processing of large files.

```javascript
const fs = require("fs");

// Copying a file using file streams
const readStream = fs.createReadStream("source.txt");
const writeStream = fs.createWriteStream("destination.txt");

readStream.pipe(writeStream);

console.log("Started streaming file copy...");
```

---

## 🗺️ 3.2. Path (`path` module)

Different operating systems use different path separators (`/` for Mac/Linux, `\` for Windows). The `path` module helps you build file paths that work correctly on any system, ensuring cross-platform compatibility.

### Working with File Paths:

The `path.join()` method is essential. It takes multiple path segments as arguments and joins them into a single, normalized, cross-platform-safe path.

```javascript
const path = require("path");

// __dirname is a global variable in Node.js that represents the directory name of the current module.
const filePath = path.join(__dirname, "public", "assets", "images", "logo.png");
console.log("Cross-platform file path:", filePath);
// On Windows: C:\path\to\your\app\public\assets\images\logo.png
// On Mac/Linux: /path/to/your/app/public/assets/images/logo.png

const parsedPath = path.parse(filePath);
console.log("Parsed path:", parsedPath);
/*
{
  root: '/', // or 'C:\' on Windows
  dir: '/path/to/your/app/public/assets/images',
  base: 'logo.png',
  ext: '.png',
  name: 'logo'
}
*/

const resolvedPath = path.resolve("data", "users.json");
console.log("Resolved path:", resolvedPath);
// Resolves a sequence of paths or path segments into an absolute path.
```

---

## 🌐 3.3. HTTP (`http` module)

This is the foundational module for all networking in Node.js. You use it to create powerful web servers.

### Creating a Simple Web Server:

The `http.createServer()` method creates a server that listens for incoming requests.

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
  // This callback runs every time a request comes in
  console.log(`Request received for: ${req.url}`);

  // Set the response HTTP header with HTTP status and Content-Type
  res.writeHead(200, { "Content-Type": "text/plain" });

  // Send the response body "Hello World"
  res.end("Hello World from Node.js HTTP Server!\n");
});

const PORT = 3000;
server.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
  console.log("Press Ctrl+C to stop the server.");
});
```

### Handling Requests and Responses:

The server's callback function receives two crucial objects:

- `request` (`req`): Contains information about the incoming client request (e.g., URL, HTTP method, headers, body).
- `response` (`res`): Used to send data back to the client (e.g., set status codes, headers, and send the response body).

You can check the request URL (`req.url`) to send back different content or perform different actions based on the requested path.

```javascript
const http = require("http");

const server = http.createServer((req, res) => {
  if (req.url === "/") {
    res.writeHead(200, { "Content-Type": "text/html" });
    res.end("<h1>Welcome to the homepage!</h1>");
  } else if (req.url === "/about") {
    res.writeHead(200, { "Content-Type": "text/plain" });
    res.end("This is the about page.");
  } else if (req.url === "/api/users") {
    res.writeHead(200, { "Content-Type": "application/json" });
    const users = [
      { id: 1, name: "Alice" },
      { id: 2, name: "Bob" },
    ];
    res.end(JSON.stringify(users));
  } else {
    res.writeHead(404, { "Content-Type": "text/plain" });
    res.end("404 Not Found");
  }
});

server.listen(8080, () => {
  console.log("Server listening on http://localhost:8080");
});
```

---

## 💻 3.4. OS and Process

These modules let you interact with the underlying operating system and the current Node.js process itself.

### Accessing Operating System Information (`os`):

The `os` module provides details about the host machine, such as CPU information (`os.cpus()`), total and free memory (`os.totalmem()`, `os.freemem()`), the operating system platform (`os.platform()`), network interfaces (`os.networkInterfaces()`), and more.

```javascript
const os = require("os");

console.log("OS Platform:", os.platform());
console.log("Architecture:", os.arch());
console.log("Total Memory (MB):", (os.totalmem() / 1024 / 1024).toFixed(2));
console.log("Free Memory (MB):", (os.freemem() / 1024 / 1024).toFixed(2));
console.log("CPU Info:", os.cpus()[0].model);
console.log("Uptime (seconds):", os.uptime());
```

### Working with the Current Process (`process`):

The `process` object is a **global** object that gives you information about and control over the currently running Node.js instance. You don't need to `require` it.

Key properties and methods include:

- **`process.env`**: An object containing all environment variables visible to the Node.js process. This is critical for storing configuration settings (like database URLs, API keys, port numbers) and **secrets** without hardcoding them into your application code.

  ```javascript
  // To run: PORT=4000 node app.js
  const PORT = process.env.PORT || 3000;
  console.log(`Application running on port: ${PORT}`);

  // Accessing a custom environment variable
  // To run: DB_HOST=localhost node app.js
  console.log("Database Host:", process.env.DB_HOST);
  ```

- **`process.argv`**: An array containing the command-line arguments passed when the Node.js script was launched. The first element is `node`, the second is the path to the script, and subsequent elements are any additional arguments.

  ```javascript
  // To run: node app.js arg1 arg2
  console.log("Command-line arguments:", process.argv);
  // Output: [ '/path/to/node', '/path/to/app.js', 'arg1', 'arg2' ]

  const customArg = process.argv[2];
  if (customArg) {
    console.log("First custom argument:", customArg);
  }
  ```

- **`process.exit(code)`**: A function to terminate the Node.js application immediately. The optional `code` argument (an integer) indicates the exit status; `0` typically means success, while non-zero values indicate an error.

  ```javascript
  console.log("Doing some work...");
  // Simulate an error condition
  const hasError = true;
  if (hasError) {
    console.error("An unrecoverable error occurred!");
    process.exit(1); // Exit with a non-zero code indicating failure
  }
  console.log("Work completed successfully."); // This line will not be reached if process.exit(1) is called
  ```

# Part 2: Building with Express.js

---

## 🚀 Chapter 4: Introduction to Express.js

### 4.1. What is Express.js?

**Express.js** is a fast, unopinionated, minimalist web framework for Node.js. It provides a robust set of features for web and mobile applications. It's the de facto standard for building web servers with Node.js.

#### Why Use a Framework?

While you can build web applications using Node.js's built-in `http` module, a framework like Express.js significantly simplifies development by:

- **Streamlining Routing**: Easily define how your application responds to different HTTP methods and URLs.
- **Handling Middleware**: A powerful mechanism to execute functions at various stages of the request-response cycle.
- **Simplifying Request and Response Handling**: Provides convenient methods for working with request data and sending various types of responses.
- **Enhancing Scalability**: Promotes modular and organized code.
- **Ecosystem**: Benefits from a vast ecosystem of third-party packages that extend its functionality.

### 🛠️ 4.2. Setting Up Your First Express Server

Let's get an Express server up and running\!

1.  **Initialize your project**:
    ```bash
    mkdir my-express-app
    cd my-express-app
    npm init -y
    ```
2.  **Install Express**:
    ```bash
    npm install express
    ```
3.  **Create your main application file** (e.g., `app.js` or `server.js`):

    ```javascript
    // app.js
    const express = require("express"); // Import the express module
    const app = express(); // Create an Express application instance
    const PORT = process.env.PORT || 3000; // Define the port, defaulting to 3000

    // Define a simple route for the root URL
    app.get("/", (req, res) => {
      res.send("Hello from your first Express server!");
    });

    // Start the server and listen for incoming requests
    app.listen(PORT, () => {
      console.log(`Server is running on port ${PORT}`);
      console.log(`Access it at http://localhost:${PORT}`);
    });
    ```

4.  **Run your server**:
    ```bash
    node app.js
    ```
    ✅ You should see "Server is running on port 3000" in your terminal. Open your browser and navigate to `http://localhost:3000` to see "Hello from your first Express server\!".

### 🗺️ 4.3. Basic Routing

**Routing** refers to how an application responds to a client request to a particular endpoint, which is a URI (or path) and a specific HTTP method (GET, POST, etc.).

#### HTTP Methods (GET, POST, PUT, DELETE)

Express provides methods corresponding to HTTP verbs to define routes:

- **`app.get(path, handler)`**: Handles HTTP GET requests. Used to retrieve data.
- **`app.post(path, handler)`**: Handles HTTP POST requests. Used to submit data to be processed to a specified resource.
- **`app.put(path, handler)`**: Handles HTTP PUT requests. Used to update a resource.
- **`app.delete(path, handler)`**: Handles HTTP DELETE requests. Used to delete a resource.
- **`app.all(path, handler)`**: Handles all HTTP methods for a specified path.
- **`app.use(path, handler)`**: Used for middleware, often to apply logic to all incoming requests or to requests matching a certain path prefix.

<!-- end list -->

```javascript
// Example routes using different HTTP methods
app.get("/users", (req, res) => {
  res.send("GET request to /users - List of users");
});

app.post("/users", (req, res) => {
  res.send("POST request to /users - Create a new user");
});

app.put("/users/:id", (req, res) => {
  res.send(`PUT request to /users/${req.params.id} - Update user`);
});

app.delete("/users/:id", (req, res) => {
  res.send(`DELETE request to /users/${req.params.id} - Delete user`);
});
```

#### Route Parameters

Route parameters are named URL segments that are used to capture the values specified at their position in the URL. They are typically used to identify specific resources. Express captures these values in `req.params`.

```javascript
app.get("/users/:userId/books/:bookId", (req, res) => {
  const userId = req.params.userId;
  const bookId = req.params.bookId;
  res.send(`Fetching book ${bookId} for user ${userId}`);
});

// Example usage: GET /users/123/books/abc
// req.params will be { userId: '123', bookId: 'abc' }
```

#### Query Strings

Query strings are appended to the URL after a `?` and consist of key-value pairs (e.g., `?name=Alice&age=30`). They are used to filter, sort, or paginate data. Express parses them into `req.query`.

```javascript
app.get("/products", (req, res) => {
  const category = req.query.category;
  const sortBy = req.query.sortBy;
  res.send(
    `Products filtered by category: ${category || "none"} and sorted by: ${
      sortBy || "default"
    }`
  );
});

// Example usage: GET /products?category=electronics&sortBy=price
// req.query will be { category: 'electronics', sortBy: 'price' }
```

### 💬 4.4. Handling Requests and Responses

The core of an Express route handler involves interacting with the `request` (`req`) and `response` (`res`) objects.

#### The `request` and `response` Objects

- **`req` (Request Object)**: Represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, etc.
  - `req.params`: Route parameters.
  - `req.query`: Query string parameters.
  - `req.body`: Request body (requires middleware like `express.json()`).
  - `req.headers`: Request headers.
  - `req.method`: HTTP method (e.g., 'GET', 'POST').
  - `req.url`: Request URL.
- **`res` (Response Object)**: Represents the HTTP response that an Express app sends when it gets an HTTP request.
  - `res.send(body)`: Sends an HTTP response. The `body` can be a String, Buffer, an object, or an array. Express automatically sets the `Content-Type`.
  - `res.json(body)`: Sends a JSON response. Sets `Content-Type` to `application/json`.
  - `res.status(code)`: Sets the HTTP status for the response.
  - `res.sendFile(path)`: Transfers the file at the given `path`.
  - `res.render(view, locals)`: Renders a view template (requires a template engine).
  - `res.redirect(path)`: Redirects a request.

#### Sending JSON, HTML, and Files

```javascript
// Sending JSON
app.get("/api/data", (req, res) => {
  const data = {
    message: "This is some JSON data",
    timestamp: new Date().toISOString(),
  };
  res.json(data); // Automatically sets Content-Type: application/json
});

// Sending HTML
app.get("/html-page", (req, res) => {
  res.send(
    "<!DOCTYPE html><html><head><title>My Page</title></head><body><h1>Hello HTML!</h1></body></html>"
  );
  // Alternatively, use res.sendFile to send an HTML file
  // res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

// Sending Files (e.g., images, PDFs, static HTML files)
const path = require("path");
app.get("/download/report.pdf", (req, res) => {
  const filePath = path.join(__dirname, "files", "report.pdf"); // Assuming 'files' directory exists
  res.sendFile(filePath, (err) => {
    if (err) {
      console.error("Error sending file:", err);
      res.status(500).send("Could not send file.");
    }
  });
});
```

---

## ⚙️ Chapter 5: Middleware in Express.js

### 5.1. What is Middleware?

**Middleware** functions are functions that have access to the `request` object (`req`), the `response` object (`res`), and the `next` middleware function in the application's request-response cycle. The `next` function is a function in the Express router which, when invoked, executes the next middleware function in the stack.

Middleware functions can:

- Execute any code.
- Make changes to the request and the response objects.
- End the request-response cycle.
- Call the next middleware in the stack.

Think of middleware as a series of steps your request goes through before it reaches its final route handler, or on its way back as a response.

```javascript
// A basic middleware function
app.use((req, res, next) => {
  console.log("Time:", Date.now());
  next(); // Pass control to the next middleware function
});

app.get("/dashboard", (req, res) => {
  res.send("Welcome to the dashboard!");
});
```

✅ **Order Matters**: Middleware functions are executed in the order they are defined.

### ✍️ 5.2. Writing Custom Middleware

You can write your own middleware functions to perform specific tasks, such as authentication, logging, or input validation.

```javascript
// Custom logging middleware
const requestLogger = (req, res, next) => {
  console.log(`${req.method} ${req.url} at ${new Date().toISOString()}`);
  next(); // Don't forget to call next()!
};

// Custom authentication middleware
const authenticateUser = (req, res, next) => {
  const isAuthenticated = true; // Replace with actual authentication logic (e.g., check token)
  if (isAuthenticated) {
    req.user = { id: 1, name: "John Doe" }; // Attach user info to request
    next();
  } else {
    res.status(401).send("Unauthorized");
  }
};

// Apply middleware globally
app.use(requestLogger);

// Apply middleware to specific routes
app.get("/protected", authenticateUser, (req, res) => {
  res.send(`Welcome, ${req.user.name}! This is protected content.`);
});
```

### 📦 5.3. Using Built-in Middleware

Express comes with several built-in middleware functions for common tasks.

- **`express.json()`**: Parses incoming requests with JSON payloads. It populates `req.body` with the parsed JSON data.

  ```javascript
  app.use(express.json()); // Essential for handling JSON in POST/PUT requests

  app.post("/api/items", (req, res) => {
    const newItem = req.body; // newItem will contain the JSON data
    console.log("Received new item:", newItem);
    res.status(201).json({ message: "Item created", item: newItem });
  });
  ```

- **`express.urlencoded()`**: Parses incoming requests with URL-encoded payloads (typically from HTML forms). It populates `req.body` with the parsed data.

  ```javascript
  app.use(express.urlencoded({ extended: true })); // 'extended: true' allows rich objects and arrays to be encoded

  app.post("/submit-form", (req, res) => {
    const formData = req.body; // formData will contain the form data
    console.log("Received form data:", formData);
    res.send("Form submitted successfully!");
  });
  ```

- **`express.static()`**: Serves static files such as images, CSS files, and JavaScript files from a specified directory.

  ```javascript
  const path = require("path");
  app.use(express.static(path.join(__dirname, "public"))); // Serves files from the 'public' directory

  // Now, a request to /styles.css will serve public/styles.css
  // A request to /images/logo.png will serve public/images/logo.png
  ```

  💡 **Tip**: Place your `express.static()` middleware _before_ your routes, so static files are served directly without hitting your route handlers.

### 🌐 5.4. Third-Party Middleware (e.g., `cors`, `morgan`)

The Express ecosystem thrives on a vast collection of third-party middleware available on npm.

- **`cors`**: Enables Cross-Origin Resource Sharing (CORS). Essential for allowing web browsers from different domains to make requests to your API.

  ```bash
  npm install cors
  ```

  ```javascript
  const cors = require("cors");
  app.use(cors()); // Allow all CORS requests

  // Or configure for specific origins:
  // app.use(cors({ origin: 'http://localhost:8080' }));
  ```

- **`morgan`**: A popular HTTP request logger middleware for Node.js. It logs incoming requests to the console, which is very helpful for debugging.

  ```bash
  npm install morgan
  ```

  ```javascript
  const morgan = require("morgan");
  app.use(morgan("dev")); // Use the 'dev' format for concise output in development

  // Other formats include 'tiny', 'short', 'common', 'combined'
  // app.use(morgan(':method :url :status :res[content-length] - :response-time ms'));
  ```

### 🚫 5.5. Error Handling Middleware

Error handling in Express is done by defining middleware functions with four arguments: `(err, req, res, next)`. When an error occurs, Express will skip all regular middleware and routing functions and execute the error handling middleware.

```javascript
// Generic error handling middleware - MUST be the last middleware in your stack
app.use((err, req, res, next) => {
  console.error(err.stack); // Log the error stack for debugging
  res.status(500).send("Something broke!"); // Send a generic error response
});

// Example route that might throw an error
app.get("/buggy-route", (req, res, next) => {
  try {
    throw new Error("Something went wrong in the buggy route!");
  } catch (error) {
    next(error); // Pass the error to the error handling middleware
  }
});
```

✅ **Best Practice**: Always define your error-handling middleware **after** all your regular routes and other `app.use()` calls.

---

## 🌳 Chapter 6: Advanced Routing and Organization

### 6.1. Using the Express Router

As your application grows, defining all routes in a single `app.js` file becomes unmanageable. The **Express Router** allows you to create modular, mountable route handlers. A `Router` instance is a complete middleware and routing system; for this reason, it is often referred to as a "mini-app."

```javascript
// routes/userRoutes.js
const express = require("express");
const router = express.Router(); // Create a new router instance

// Middleware specific to this router
router.use((req, res, next) => {
  console.log("Time: ", Date.now());
  next();
});

// Define routes on the router
router.get("/", (req, res) => {
  res.send("Get all users");
});

router.post("/", (req, res) => {
  res.send("Create a new user");
});

router.get("/:id", (req, res) => {
  res.send(`Get user with ID: ${req.params.id}`);
});

module.exports = router; // Export the router

// app.js
const userRoutes = require("./routes/userRoutes");
// ... other app.use statements ...
app.use("/api/users", userRoutes); // Mount the router at a specific path

// Now, GET /api/users will be handled by userRoutes.get('/')
// POST /api/users will be handled by userRoutes.post('/')
// GET /api/users/123 will be handled by userRoutes.get('/:id')
```

💡 **Benefit**: This promotes cleaner code, better organization, and easier maintenance.

### 🏗️ 6.2. Structuring Your Application (Controllers, Services, Routes)

For larger applications, it's highly recommended to adopt a structured approach, separating concerns into different layers:

- **`routes/`**: Contains route definitions (using `express.Router()`). These files map URLs to controller functions.
- **`controllers/`**: Contains the logic for handling incoming requests and preparing responses. They interact with services.
- **`services/`** (or `models/` or `data-access/`): Contains the business logic and interacts directly with the database. This layer abstracts database operations from the controllers.
- **`models/`**: (If using ORMs/ODMs like Mongoose/Sequelize) Defines database schemas/models.

<!-- end list -->

```
my-express-app/
├── app.js             // Main application file
├── package.json
├── node_modules/
├── routes/
│   └── userRoutes.js
│   └── productRoutes.js
├── controllers/
│   └── userController.js
│   └── productController.js
├── services/
│   └── userService.js
│   └── productService.js
├── models/            // For Mongoose/Sequelize schemas/models
│   └── User.js
│   └── Product.js
└── public/            // For static assets
    ├── index.html
    └── css/
```

**Example Flow:**

1.  **Request comes in:** `GET /api/users`
2.  **`app.js`**: Routes the request to `userRoutes.js`.
3.  **`userRoutes.js`**: `router.get('/', userController.getAllUsers);` directs it to `userController.getAllUsers`.
4.  **`userController.js`**: `getAllUsers` calls `userService.findAllUsers()`.
5.  **`userService.js`**: `findAllUsers` interacts with the `User` model (e.g., `User.find()`) and returns data.
6.  **`userController.js`**: Receives data from `userService`, formats it, and sends the `res.json(data)`.

### 🔗 6.3. Route Groups and Prefixes

Using `express.Router()` naturally creates route groups with prefixes when you mount them using `app.use()`.

```javascript
// app.js
const express = require("express");
const app = express();
const userRoutes = require("./routes/userRoutes");
const productRoutes = require("./routes/productRoutes");

// All routes defined in userRoutes will be prefixed with '/api/users'
app.use("/api/users", userRoutes);

// All routes defined in productRoutes will be prefixed with '/api/products'
app.use("/api/products", productRoutes);

// Example: routes/userRoutes.js has:
// router.get('/', ...) => handles GET /api/users
// router.get('/:id', ...) => handles GET /api/users/:id
```

This approach keeps your main `app.js` clean and makes your API structure clear.

---

# Part 3: Data and Databases

So far, our applications have been stateless; any data they handle disappears when the server restarts. To build real-world applications, you need to store data persistently. This is where databases come in. This part covers how to connect your Node.js application to popular databases and how to generate dynamic HTML on the server.

---

## 🗄️ Chapter 7: Working with Databases

This chapter explores how Node.js applications interact with databases to store, retrieve, and manage data.

### 7.1. Introduction to Databases in Node.js

Node.js itself doesn't include a database. Instead, it connects to existing database systems using libraries called **drivers** (or **clients**). You can connect to virtually any database from a Node.js application.

There are two main categories of databases you'll encounter:

- **SQL (Relational) Databases**:

  - **Examples**: PostgreSQL, MySQL, SQLite, Microsoft SQL Server.
  - **Structure**: Store data in a structured way using **tables** with rows and columns.
  - **Schema**: Enforce a predefined schema (e.g., each row in a table must have specific columns with specific data types).
  - **Query Language**: Use the **Structured Query Language (SQL)** for queries (e.g., `SELECT * FROM users WHERE age > 25;`).
  - **Characteristics**: Known for their reliability, strong data consistency (ACID properties), and mature ecosystems. Best for applications requiring complex queries and transactions.

- **NoSQL (Non-relational) Databases**:

  - **Examples**: MongoDB (Document), Redis (Key-Value), Cassandra (Column-Family), Neo4j (Graph).
  - **Structure**: This is a broad category of databases that don't use the traditional table structure.
  - **Document Databases (like MongoDB)**: Store data in flexible, JSON-like **documents**. Documents can have varying structures within the same collection.
  - **Schema**: Often schema-less or flexible schema.
  - **Query Language**: Varies by database (e.g., MongoDB uses a JSON-based query language).
  - **Characteristics**: Known for their horizontal scalability, flexibility (easy to change data structures), and performance for certain workloads. Best for applications with rapidly changing data requirements, large datasets, or real-time needs.

To make working with databases easier and more object-oriented, developers often use:

- **ORM (Object-Relational Mapper)** for SQL databases (e.g., **Sequelize**, TypeORM, Prisma).
- **ODM (Object-Data Mapper)** for NoSQL databases (e.g., **Mongoose** for MongoDB).

These libraries let you interact with your database using familiar JavaScript objects and methods instead of writing raw database queries. This reduces boilerplate code and helps prevent common issues like SQL injection.

### 🍃 7.2. Connecting to a MongoDB Database (with Mongoose)

MongoDB is the most popular NoSQL document database, and **Mongoose** is the go-to library for using it with Node.js. Mongoose helps by providing schema validation, type casting, query building, and business logic hooks, making MongoDB interaction much more manageable.

First, install Mongoose:

```bash
npm install mongoose
```

Next, connect to your MongoDB database in your main application file (e.g., `app.js` or `server.js`):

```javascript
// app.js or db.js
const mongoose = require("mongoose");

// Replace with your MongoDB connection string.
// 'mongodb://localhost:27017' is the default for a local MongoDB instance.
// 'my-app' is the name of the database you want to connect to.
const mongoURI = "mongodb://localhost:27017/my-app";

mongoose
  .connect(mongoURI, {
    // Optional: Recommended options for new connection management
    // useNewUrlParser: true,
    // useUnifiedTopology: true,
    // useCreateIndex: true, // No longer supported in Mongoose 6+
    // useFindAndModify: false // No longer supported in Mongoose 6+
  })
  .then(() => console.log("✅ MongoDB connected successfully!"))
  .catch((err) => console.error("❌ MongoDB connection error:", err));

// It's good practice to handle connection events
mongoose.connection.on("error", (err) => {
  console.error("MongoDB connection error event:", err);
});

mongoose.connection.on("disconnected", () => {
  console.log("MongoDB disconnected!");
});

// To close the connection when the app exits
process.on("SIGINT", async () => {
  await mongoose.connection.close();
  console.log("MongoDB connection closed due to app termination");
  process.exit(0);
});
```

💡 **Important**: In a production environment, your `mongoURI` should be stored in an environment variable (e.g., `process.env.MONGO_URI`) for security and flexibility.

#### Defining Schemas and Models

In Mongoose, everything starts with a **Schema**. A `Schema` defines the structure of the documents within a collection—what fields they have, what type of data those fields hold, and any validation rules.

A **Model** is a wrapper around the `Schema`. It provides a structured interface for creating, reading, updating, and deleting documents (**CRUD operations**) in the database.

**Example: Creating a User Schema and Model**

Create a file for your model, e.g., `models/User.js`:

```javascript
// models/User.js
const { Schema, model } = require("mongoose");

// Define the schema for a User
const userSchema = new Schema(
  {
    name: {
      type: String,
      required: true,
      trim: true, // Trims whitespace from the beginning and end of the string
    },
    email: {
      type: String,
      required: true,
      unique: true, // Ensures email addresses are unique
      lowercase: true, // Converts email to lowercase before saving
      match: [/.+@.+\..+/, "Please fill a valid email address"], // Basic email validation
    },
    age: {
      type: Number,
      min: [18, "Must be at least 18 years old"], // Minimum age validation
      max: [120, "Age cannot exceed 120"], // Maximum age validation
    },
    isActive: {
      type: Boolean,
      default: true, // Default value if not provided
    },
    registrationDate: {
      type: Date,
      default: Date.now, // Default to current date
    },
  },
  {
    timestamps: true, // Automatically adds `createdAt` and `updatedAt` fields
  }
);

// Add a custom method to the schema (optional)
userSchema.methods.findSimilarAgeUsers = function (cb) {
  return model("User").find({ age: this.age }, cb);
};

// Add a static method to the schema (optional)
userSchema.statics.findByEmail = function (email) {
  return this.findOne({ email: email });
};

// Create a model from the schema
const User = model("User", userSchema); // 'User' will be the collection name (pluralized to 'users')

module.exports = User;
```

#### CRUD Operations

**CRUD** stands for **Create, Read, Update, Delete**. Here's how you perform these basic operations with a Mongoose model.

Assume you have `models/User.js` as defined above.

```javascript
// In a separate file (e.g., scripts/manageUsers.js or in a route handler)
const User = require("./models/User"); // Assuming the model is in a separate file
require("./app"); // Ensure MongoDB connection is established

async function manageUsers() {
  try {
    // --- CREATE ---
    console.log("\n--- CREATE ---");
    const newUser = await User.create({
      name: "Jane Doe",
      email: "jane.doe@example.com",
      age: 25,
    });
    console.log("✅ User created:", newUser);

    const anotherUser = await User.create({
      name: "John Smith",
      email: "john.smith@example.com",
      age: 30,
    });
    console.log("✅ Another user created:", anotherUser);

    // --- READ ---
    console.log("\n--- READ ---");
    // Find all users
    const allUsers = await User.find();
    console.log("All users:", allUsers);

    // Find users by a specific condition
    const usersOver28 = await User.find({ age: { $gt: 28 } });
    console.log("Users over 28:", usersOver28);

    // Find one user by ID
    const singleUser = await User.findById(newUser._id);
    console.log("Single user (by ID):", singleUser);

    // Find one user by a field
    const userByEmail = await User.findOne({ email: "jane.doe@example.com" });
    console.log("User by email:", userByEmail);

    // --- UPDATE ---
    console.log("\n--- UPDATE ---");
    // Find and update a single user
    const updatedUser = await User.findByIdAndUpdate(
      newUser._id,
      { age: 26, name: "Jane D. Updated" },
      { new: true, runValidators: true } // `new: true` returns the updated document, `runValidators: true` runs schema validators on update
    );
    console.log("Updated user:", updatedUser);

    // Update multiple documents
    const updateResult = await User.updateMany(
      { age: { $gt: 29 } },
      { $inc: { age: 1 } } // Increment age by 1 for users older than 29
    );
    console.log("Documents updated:", updateResult.modifiedCount);

    // --- DELETE ---
    console.log("\n--- DELETE ---");
    // Find and delete a single user
    const deletedUser = await User.findByIdAndDelete(newUser._id);
    console.log("Deleted user (by ID):", deletedUser);

    // Delete multiple documents
    const deleteResult = await User.deleteMany({ name: "John Smith" });
    console.log("Documents deleted:", deleteResult.deletedCount);

    const remainingUsers = await User.find();
    console.log("Remaining users:", remainingUsers);
  } catch (error) {
    console.error("An error occurred during user management:", error.message);
  } finally {
    // Disconnect from MongoDB when operations are done (important for scripts, not for always-running servers)
    // await mongoose.connection.close();
    // console.log('MongoDB connection closed.');
  }
}

manageUsers();
```

💡 **Asynchronous Nature**: All Mongoose operations are asynchronous and return Promises, making `async/await` the ideal way to handle them.

### 🐘 7.3. Connecting to a SQL Database (with Sequelize)

**Sequelize** is a popular promise-based ORM (Object-Relational Mapper) for Node.js that supports databases like PostgreSQL, MySQL, MariaDB, SQLite, and Microsoft SQL Server. It lets you define models that map to your database tables and interact with your database using JavaScript objects and methods instead of raw SQL.

First, install Sequelize and the driver for your chosen database (e.g., `pg` for PostgreSQL, `mysql2` for MySQL, `sqlite3` for SQLite):

```bash
npm install sequelize pg # For PostgreSQL
# npm install sequelize mysql2 # For MySQL
# npm install sequelize sqlite3 # For SQLite
```

Next, set up the connection:

```javascript
// db.js or config/database.js
const { Sequelize } = require("sequelize");

// Create a new Sequelize instance
// Example for PostgreSQL
const sequelize = new Sequelize("my_database", "my_user", "my_password", {
  host: "localhost",
  dialect: "postgres", // Specify the dialect
  port: 5432, // Default PostgreSQL port
  logging: false, // Set to true to see SQL queries in console
});

// Example for MySQL
// const sequelize = new Sequelize('my_database', 'root', 'password', {
//   host: 'localhost',
//   dialect: 'mysql'
// });

// Example for SQLite (file-based database)
// const sequelize = new Sequelize({
//   dialect: 'sqlite',
//   storage: 'database.sqlite' // The file where the database will be stored
// });

// Test the connection
async function testConnection() {
  try {
    await sequelize.authenticate();
    console.log(
      "✅ Connection to SQL database has been established successfully."
    );
  } catch (error) {
    console.error("❌ Unable to connect to the database:", error);
  }
}

testConnection();

module.exports = sequelize; // Export the instance for use in models
```

💡 **Production Reminder**: Database credentials (`username`, `password`, `host`) should always be stored in environment variables (e.g., `process.env.DB_USER`, `process.env.DB_PASS`) and not hardcoded.

#### Defining Models and Migrations

In Sequelize, a **Model** represents a table in your database. You define the model's name and its columns with their data types.

**Migrations** are a critical concept in SQL development. They are JavaScript files that contain code to alter your database schema (e.g., creating a table, adding a new column, modifying a column, deleting a table). Migrations allow you to evolve your database structure over time in a controlled and versioned way, which is essential for teamwork and deploying changes.

Sequelize has a companion CLI tool (`sequelize-cli`) to manage migrations, which is highly recommended for production applications.

```bash
npm install -g sequelize-cli # Install globally
# or locally: npm install --save-dev sequelize-cli
```

Then, initialize it: `sequelize init`. This will create `config`, `migrations`, `models`, and `seeders` folders.

**Example: A User Model**

Create a file for your model, e.g., `models/User.js`:

```javascript
// models/User.js
const { DataTypes } = require("sequelize");
const sequelize = require("../db"); // Assuming db.js exports the sequelize instance

const User = sequelize.define(
  "User",
  {
    // Model attributes are defined here
    id: {
      type: DataTypes.INTEGER,
      autoIncrement: true,
      primaryKey: true,
    },
    firstName: {
      type: DataTypes.STRING,
      allowNull: false,
    },
    lastName: {
      type: DataTypes.STRING,
      defaultValue: "Doe", // Default value if not provided
    },
    email: {
      type: DataTypes.STRING,
      unique: true, // Ensures email is unique
      validate: {
        isEmail: true, // Sequelize built-in validator
      },
    },
    age: {
      type: DataTypes.INTEGER,
      validate: {
        min: 18, // Minimum value validator
      },
    },
  },
  {
    // Other model options go here
    timestamps: true, // Adds createdAt and updatedAt columns
    tableName: "users", // Explicitly set table name if different from model name pluralized
  }
);

// `sequelize.sync()` creates the table if it doesn't exist (DANGEROUS for production!)
// This is good for development/testing, but for production, you should ALWAYS use migrations.
(async () => {
  // `sync({ force: true })` will drop the table if it already exists, then re-create it.
  // Use with extreme caution, as it will DELETE ALL DATA.
  // await User.sync({ force: true });
  await User.sync(); // This will create the table if it doesn't exist.
  console.log("✅ User table synced (created if not exists).");
})();

module.exports = User;
```

#### CRUD Operations

Here's how you perform the four basic database operations with a Sequelize model.

Assume you have `models/User.js` defined as above and `db.js` connecting to the database.

```javascript
// In a separate file (e.g., scripts/manageUsersSQL.js or in a route handler)
const User = require("./models/User"); // Assuming the model is in a separate file
require("./db"); // Ensure SQL database connection is established and model is synced

async function manageUsersSQL() {
  try {
    // --- CREATE ---
    console.log("\n--- CREATE ---");
    const jane = await User.create({
      firstName: "Jane",
      lastName: "Doe",
      email: "jane.doe@example.com",
      age: 25,
    });
    console.log("✅ Jane's auto-generated ID:", jane.id);

    const john = await User.create({
      firstName: "John",
      lastName: "Smith",
      email: "john.smith@example.com",
      age: 30,
    });
    console.log("✅ John's auto-generated ID:", john.id);

    // --- READ ---
    console.log("\n--- READ ---");
    // Find all users
    const users = await User.findAll();
    console.log(
      "All users:",
      users.map((u) => u.toJSON())
    ); // .toJSON() converts Sequelize instance to plain object

    // Find by Primary Key (ID)
    const singleUser = await User.findByPk(jane.id);
    console.log(
      "Single user (by ID):",
      singleUser ? singleUser.toJSON() : "Not found"
    );

    // Find one user by a condition
    const userByEmail = await User.findOne({
      where: { email: "john.smith@example.com" },
    });
    console.log(
      "User by email:",
      userByEmail ? userByEmail.toJSON() : "Not found"
    );

    // Find users with specific attributes, ordered
    const youngUsers = await User.findAll({
      where: { age: { [Sequelize.Op.lt]: 30 } }, // Op.lt means 'less than'
      order: [["firstName", "ASC"]],
    });
    console.log(
      "Young users (age < 30):",
      youngUsers.map((u) => u.toJSON())
    );

    // --- UPDATE ---
    console.log("\n--- UPDATE ---");
    // Update an instance (first retrieve, then update)
    jane.lastName = "Smith";
    await jane.save(); // Save changes to the database
    console.log("✅ Jane was updated:", jane.toJSON());

    // Update multiple records with a condition
    const [affectedRows] = await User.update(
      { age: Sequelize.literal("age + 1") }, // Increment age by 1
      { where: { lastName: "Smith" } }
    );
    console.log(`Updated ${affectedRows} users.`);

    const updatedJohn = await User.findByPk(john.id);
    console.log(
      "Updated John:",
      updatedJohn ? updatedJohn.toJSON() : "Not found"
    );

    // --- DELETE ---
    console.log("\n--- DELETE ---");
    // Delete an instance
    await jane.destroy();
    console.log("✅ Jane was deleted");

    // Delete records with a condition
    const deletedCount = await User.destroy({
      where: { age: { [Sequelize.Op.gt]: 30 } }, // Delete users older than 30
    });
    console.log(`Deleted ${deletedCount} users.`);

    const remainingUsers = await User.findAll();
    console.log(
      "Remaining users:",
      remainingUsers.map((u) => u.toJSON())
    );
  } catch (error) {
    console.error(
      "❌ An error occurred during SQL user management:",
      error.message
    );
  } finally {
    // It's not typically necessary to close the connection in a persistent server app,
    // but useful for standalone scripts.
    // await sequelize.close();
    // console.log('SQL connection closed.');
  }
}

manageUsersSQL();
```

💡 **Sequelize Operators**: For complex queries (like greater than, less than, like), Sequelize uses `Sequelize.Op` (operators). Remember to import `Sequelize` from the `sequelize` package when using them.

---

## 🎨 Chapter 8: Template Engines

When you want to send back HTML from your Express server, you could manually build HTML strings, but that's messy and inefficient, especially for dynamic content. **Template engines** provide a much better way to generate HTML dynamically on the server. This is known as **Server-Side Rendering (SSR)**.

### 8.1. What are Template Engines?

A template engine lets you write a "**template**"—a file that looks like HTML but with special placeholders and logic (e.g., loops, conditional statements). When a user makes a request, your Express server combines this template with **dynamic data** (e.g., user information from the database) to produce a final, standard HTML document, which it then sends to the browser.

To use a template engine in Express, you need to:

1.  **Install the engine's package** (e.g., `npm install ejs`).
2.  **Set it as the view engine in Express**: `app.set('view engine', 'ejs');`.
3.  **Create a `views` folder** in your project root to store your template files (Express looks for templates here by default).
4.  **Render a template** using `res.render('templateName', { data });`.

### 🧩 8.2. Using EJS

**EJS (Embedded JavaScript)** is a very popular template engine because of its simplicity: it's just HTML with the ability to embed plain JavaScript. There are no special rules to learn beyond its tags.

- **`<% ... %>`**: For running JavaScript code/logic (like loops or if-statements). The output of these tags is not displayed.
- **`<%= ... %>`**: For **outputting** the value of a variable into the HTML. This tag also **escapes** the data (converts special HTML characters like `<` to `&lt;`) to prevent **XSS (Cross-Site Scripting) attacks**, which is a crucial security measure.
- **`<%- ... %>`**: For outputting **raw, unescaped HTML**. Use this with caution, only when you are absolutely sure the content is safe and comes from a trusted source, as it can lead to XSS vulnerabilities if used improperly.

**Example: `views/profile.ejs`**

```html
<!DOCTYPE html>
<html>
  <head>
    <title><%= title %></title>
    <link rel="stylesheet" href="/css/style.css" />
  </head>
  <body>
    <h1>Welcome, <%= user.name %>!</h1>

    <% if (user.isAdmin) { %>
    <p class="admin-message">You have admin privileges. Be careful!</p>
    <% } else { %>
    <p>You are a regular user.</p>
    <% } %>

    <h3>Your Hobbies:</h3>
    <% if (hobbies && hobbies.length > 0) { %>
    <ul>
      <% hobbies.forEach(hobby => { %>
      <li><%= hobby %></li>
      <% }); %>
    </ul>
    <% } else { %>
    <p>No hobbies listed.</p>
    <% } %>

    <p>Raw HTML example (use with caution): <%- rawHtmlContent %></p>
  </body>
</html>
```

**`app.js` configuration and route:**

```javascript
// app.js
const express = require("express");
const app = express();
const path = require("path");

// 1. Install EJS: npm install ejs
// 2. Set EJS as the view engine
app.set("view engine", "ejs");
// 3. Set the views directory (optional, 'views' is default)
app.set("views", path.join(__dirname, "views"));

// Serve static files (like CSS)
app.use(express.static(path.join(__dirname, "public")));

app.get("/profile", (req, res) => {
  const userData = {
    name: "Alex",
    isAdmin: true,
    email: "alex@example.com",
  };
  const userHobbies = ["Reading", "Hiking", "Coding"];
  const dangerousHtml = "<strong>This is unescaped HTML!</strong>";

  res.render("profile", {
    title: "User Profile Page",
    user: userData,
    hobbies: userHobbies,
    rawHtmlContent: dangerousHtml, // Will be rendered unescaped by <%- ... %>
  });
});

// If you want to see a user with no hobbies
app.get("/profile/no-hobbies", (req, res) => {
  res.render("profile", {
    title: "User Profile Page",
    user: { name: "Bob", isAdmin: false },
    hobbies: [], // Empty array for hobbies
    rawHtmlContent: "<em>No raw content here.</em>",
  });
});

// Make sure your server is listening
const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
  console.log("Try visiting http://localhost:3000/profile");
});
```

### 🪓 8.3. Using Pug (formerly Jade)

**Pug** is known for its clean, concise syntax that relies on indentation rather than closing tags. This can significantly reduce the amount of code you write, but it has a steeper learning curve for those unfamiliar with indentation-based languages.

- **Syntax**: No closing tags. HTML elements are written simply as their tag name. Attributes are in parentheses `(attribute="value")`. Text content follows directly after the tag.
- **Variables**: Variables are interpolated using `= variableName`.
- **Logic**: `if`, `else`, `each` (for loops) are keywords followed by their conditions/iterations.
- **Comments**: `//` for single-line, `//-` for buffered (visible in output), `//` for unbuffered (not visible).

**Example: `views/index.pug`**

```pug
// views/index.pug
doctype html
html
  head
    title= pageTitle // Outputs escaped variable
    link(rel="stylesheet", href="/css/pug-style.css") // Attributes in parentheses
  body
    h1= message
    if user // Conditional logic
      p Welcome back, #{user.name} // String interpolation
    else
      p Welcome, guest!

    //- This is a comment that will appear in the rendered HTML
    // This is a Pug comment and will NOT appear in the rendered HTML

    ul
      each item in items // Loop through an array
        li= item
```

**`app.js` configuration and route:**

```javascript
// app.js
const express = require("express");
const app = express();
const path = require("path");

// 1. Install Pug: npm install pug
// 2. Set Pug as the view engine
app.set("view engine", "pug");
// 3. Set the views directory
app.set("views", path.join(__dirname, "views"));

// Serve static files
app.use(express.static(path.join(__dirname, "public")));

app.get("/", (req, res) => {
  res.render("index", {
    pageTitle: "Pug Page Example",
    message: "Hello from Pug!",
    user: { name: "Casey" }, // Pass user data
    items: ["Apple", "Banana", "Cherry", "Date"],
  });
});

app.get("/pug-guest", (req, res) => {
  res.render("index", {
    pageTitle: "Pug Guest Page",
    message: "Welcome!",
    user: null, // No user data
    items: [], // Empty items
  });
});

// Make sure your server is listening
const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
  console.log(
    "Try visiting http://localhost:3000/ and http://localhost:3000/pug-guest"
  );
});
```

💡 **Note**: Pug is often preferred by developers who enjoy concise syntax and don't mind a departure from traditional HTML.

### 📝 8.4. Using Handlebars

**Handlebars.js** is another powerful template engine that uses a "mustache" syntax (`{{ ... }}`). It's considered "**logic-less**" because it discourages putting complex logic directly in templates, instead encouraging the use of "**helpers**" for more advanced tasks (e.g., formatting dates, custom conditionals). This promotes cleaner separation of concerns.

You typically use the `express-handlebars` package to integrate it with Express.

```bash
npm install express-handlebars
```

**Example: `views/home.hbs`**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>{{pageTitle}}</title>
    <link rel="stylesheet" href="/css/hbs-style.css" />
  </head>
  <body>
    <h1>{{heading}}</h1>

    {{#if user}}
    <p>Hello, {{user.username}}!</p>
    {{else}}
    <p>Please log in.</p>
    {{/if}}

    <h2>My Items:</h2>
    <ul>
      {{#each items}}
      <li>This item is {{this}}</li>
      {{/each}} {{#unless items}}
      <li>No items to display.</li>
      {{/unless}}
    </ul>

    <p>Current Year: {{getYear}}</p>
  </body>
</html>
```

**`app.js` configuration and route:**

```javascript
// app.js
const express = require("express");
const { engine } = require("express-handlebars"); // Import 'engine' from express-handlebars
const path = require("path");
const app = express();

// 1. Install express-handlebars: npm install express-handlebars
// 2. Configure Handlebars engine
app.engine(
  "hbs",
  engine({
    extname: ".hbs", // File extension for your templates
    defaultLayout: "main", // Optional: specify a default layout file
    layoutsDir: path.join(__dirname, "views/layouts"), // Directory for layouts
    partialsDir: path.join(__dirname, "views/partials"), // Directory for partials (reusable snippets)
    helpers: {
      // Define custom helpers
      getYear: () => new Date().getFullYear(),
      eq: (a, b) => a === b, // Example comparison helper
    },
  })
);
app.set("view engine", "hbs");
app.set("views", path.join(__dirname, "views")); // Set the views directory

// Serve static files
app.use(express.static(path.join(__dirname, "public")));

app.get("/", (req, res) => {
  res.render("home", {
    pageTitle: "Handlebars Home Page",
    heading: "Welcome to our Handlebars Site!",
    user: { username: "Logan" }, // Data for the template
    items: ["Laptop", "Mouse", "Keyboard"],
  });
});

app.get("/guest-page", (req, res) => {
  res.render("home", {
    pageTitle: "Guest Handlebars Page",
    heading: "Hello, Guest!",
    user: null, // No user logged in
    items: [],
  });
});

// Make sure your server is listening
const PORT = 3000;
app.listen(PORT, () => {
  console.log(`Server running on http://localhost:${PORT}`);
  console.log(
    "Try visiting http://localhost:3000/ and http://localhost:3000/guest-page"
  );
});
```

💡 **Layouts and Partials**: Handlebars strongly supports layouts (a common wrapper for all your pages) and partials (reusable template snippets), promoting code reusability.

# Part 4: Building a REST API

While Server-Side Rendering (SSR) is useful, modern web development often separates the frontend (like a React or Vue app) from the backend. The backend's primary role becomes providing and managing data through an **API (Application Programming Interface)**. This part covers how to design, build, and secure a **REST (REpresentational State Transfer) API**, the most common standard for web APIs.

---

## 📐 Chapter 9: Designing RESTful APIs

A well-designed API is predictable, easy to use, and scalable. REST provides a set of architectural principles to achieve this.

### 9.1. Principles of REST

REST is not a strict protocol but a set of guidelines for creating scalable and stateless web services.

- **Client-Server Separation**: The client (frontend) and the server (backend) are completely separate. The client only needs to know the URI (the endpoint) of the resource. This allows you to develop the frontend and backend independently, fostering modularity and flexibility.

- **Stateless**: 🔥 This is a core principle. The server does not store any information about the client's session between requests. Every request from the client must contain all the information necessary to process it (like an authentication token). This makes the API highly scalable, as any server can handle any request without relying on previous interactions with that client.

- **Uniform Interface**: This makes the API consistent and predictable, facilitating easier adoption and understanding by developers.

  - **Use nouns for resource URIs**: Endpoints should refer to things (resources), not actions.

    - ✅ **Good**: `/users`, `/products/123`, `/orders`
    - ❌ **Bad**: `/getUsers`, `/createProduct`, `/deleteOrderById`

  - **Use HTTP methods for actions**: Use standard HTTP verbs to operate on those resources:

    - `GET /users`: Get a list of all users. (Read)
    - `GET /users/123`: Get a single user with ID 123. (Read)
    - `POST /users`: Create a new user. (Create)
    - `PUT /users/123`: Update the entire user with ID 123. (Update/Replace)
    - `PATCH /users/123`: Partially update the user with ID 123. (Partial Update - often used for specific field updates)
    - `DELETE /users/123`: Delete the user with ID 123. (Delete)

  - **Use JSON for data transfer**: Send and receive data using JSON (JavaScript Object Notation), the standard format for modern APIs due to its lightweight nature and ease of parsing in web applications.

### ⬆️ 9.2. API Versioning

As your API evolves, you will inevitably need to make breaking changes (e.g., renaming a field, changing data types, removing an endpoint). To avoid breaking existing client applications that rely on your API, you should **version your API**. The most common and straightforward method is **URI Versioning**.

You simply prefix your API routes with a version number:

- `https://api.example.com/v1/products`
- `https://api.example.com/v2/products`

When you need to make a change that is not backward-compatible, you can create a new set of routes under `/v2`, leaving the `/v1` routes untouched for older clients. This allows clients to upgrade at their own pace.

In Express, you can easily manage this with the Router:

```javascript
// app.js
const express = require("express");
const app = express();

const v1ProductRoutes = require("./routes/v1/products"); // Your product routes for API version 1
const v2ProductRoutes = require("./routes/v2/products"); // Your product routes for API version 2
const v1UserRoutes = require("./routes/v1/users"); // User routes for API version 1

// Mount routers for different API versions
app.use("/api/v1/products", v1ProductRoutes);
app.use("/api/v2/products", v2ProductRoutes);
app.use("/api/v1/users", v1UserRoutes);

// Example: routes/v1/products.js
// const router = express.Router();
// router.get('/', (req, res) => res.json({ version: 'v1', products: [] }));
// module.exports = router;

// Example: routes/v2/products.js
// const router = express.Router();
// router.get('/', (req, res) => res.json({ apiVersion: 'v2', items: [] })); // Changed field name 'products' to 'items'
// module.exports = router;

app.listen(3000, () => console.log("API server listening on port 3000"));
```

### 🚥 9.3. Status Codes and Error Handling

Using standard **HTTP status codes** is crucial for letting the client know the outcome of a request without needing to parse a custom error message. Don't just send "error" with a `200 OK` status; be specific.

#### Common Status Codes:

- **`2xx` (Success)**

  - `200 OK`: The request was successful (commonly used for `GET`, `PUT`, `PATCH`, `DELETE`).
  - `201 Created`: A new resource was successfully created (used for `POST` requests when a resource is added).
  - `204 No Content`: The server successfully processed the request, but is not returning any content (e.g., successful DELETE).

- **`4xx` (Client Error)**: Indicates that the client made a mistake.

  - `400 Bad Request`: The server cannot process the request due to a client error (e.g., malformed syntax, invalid request body JSON, missing required parameters).
  - `401 Unauthorized`: The client is not authenticated (missing or invalid authentication credentials). The client should attempt to authenticate.
  - `403 Forbidden`: The client is authenticated but is not authorized to access this resource (e.g., insufficient permissions).
  - `404 Not Found`: The requested resource could not be found on the server.
  - `405 Method Not Allowed`: The HTTP method used is not supported for the requested resource.
  - `409 Conflict`: Indicates a request conflict with the current state of the target resource (e.g., trying to create a resource that already exists with a unique ID).
  - `422 Unprocessable Entity`: The server understands the content type of the request entity, and the syntax of the request entity is correct, but it was unable to process the contained instructions (e.g., validation errors on input data).

- **`5xx` (Server Error)**: Indicates that the server encountered an error while processing a valid request.

  - `500 Internal Server Error`: A generic error for an unexpected condition on the server. This is a fallback when no more specific 5xx error code is appropriate.
  - `502 Bad Gateway`: The server, while acting as a gateway or proxy, received an invalid response from an upstream server.
  - `503 Service Unavailable`: The server is currently unable to handle the request due to a temporary overload or scheduled maintenance, which will likely be alleviated after some delay.

Your centralized error handler should send back a JSON object with a clear error message and the correct status code.

```javascript
// app.js (after all your routes)

// Catch-all for 404 Not Found errors
app.use((req, res, next) => {
  const error = new Error("Not Found");
  error.status = 404;
  next(error); // Pass to the next middleware (our error handler)
});

// Centralized error-handling middleware
// It MUST have four arguments: (err, req, res, next)
app.use((err, req, res, next) => {
  // Log the error for internal debugging, but don't expose sensitive info to client
  console.error(err.stack);

  // Set the status code based on the error or default to 500
  const statusCode = err.status || 500;

  // Send a JSON response with an error message
  res.status(statusCode).json({
    error: {
      message: err.message || "Something went terribly wrong!",
      // In production, you might only send a generic message for 500 errors
      // You could include err.status for clarity on client side too
      code: statusCode, // Optional: include the status code in the body for clarity
    },
  });
});

// Example of a route that throws a custom error
app.get("/simulate-error", (req, res, next) => {
  const customError = new Error("Invalid input data provided!");
  customError.status = 400; // Set a specific status code for this error type
  next(customError); // Pass the error to the error handling middleware
});
```

✅ **Tip**: For custom errors, you can create a custom error class that extends `Error` and includes a `status` property for better organization and clarity.

---

## 🔐 Chapter 10: Authentication and Authorization

**Authentication** is the process of verifying _who a user is_ (e.g., by checking username/password). **Authorization** is the process of determining _what an authenticated user is allowed to do_ (e.g., can they access this resource? can they perform this action?).

### 10.1. Basic Authentication

This is a simple authentication scheme built into the HTTP protocol. The client sends a username and password in the `Authorization` header, encoded in Base64.

- `Authorization: Basic <base64_encoded_username:password>`

It's **not secure** unless sent over HTTPS (to prevent snooping) and is rarely used for modern web APIs due to its inflexibility (e.g., no logout mechanism without clearing browser data) and lack of statelessness in a practical sense.

### 10.2. Session-Based Authentication (with `express-session`)

This is a stateful, traditional approach common in server-rendered applications but less ideal for stateless REST APIs.

#### How it works:

1.  A user logs in with a username and password.
2.  If the credentials are valid, the server creates a "**session**" in its memory or a database (e.g., Redis, MongoDB). This session stores user-specific data and is given a unique **Session ID**.
3.  This Session ID is sent back to the client and stored in a **cookie**.
4.  On all subsequent requests, the client's browser automatically sends the cookie with the Session ID back to the server.
5.  The server uses the Session ID from the cookie to look up the user's session data and identify them.

The `express-session` middleware makes this easy to implement in Express. However, it's **stateful**, which violates a core REST principle and can make scaling more complex (requires session affinity or a shared session store).

```bash
npm install express-session
```

```javascript
// app.js
const session = require("express-session");

app.use(
  session({
    secret: "your_secret_key_for_signing_session_id", // Secret used to sign the session ID cookie
    resave: false, // Don't save session if unmodified
    saveUninitialized: false, // Don't create session until something stored
    cookie: {
      secure: process.env.NODE_ENV === "production", // Use secure cookies in production (requires HTTPS)
      maxAge: 1000 * 60 * 60 * 24, // Session expires in 1 day
    },
  })
);

// Login route
app.post("/login", (req, res) => {
  const { username, password } = req.body;
  // In a real app, validate username/password against a database
  if (username === "user" && password === "pass") {
    req.session.userId = "123"; // Store user data in session
    req.session.username = username;
    res.send("Logged in successfully!");
  } else {
    res.status(401).send("Invalid credentials");
  }
});

// Protected route
app.get("/dashboard", (req, res) => {
  if (req.session.userId) {
    res.send(`Welcome to your dashboard, ${req.session.username}!`);
  } else {
    res.status(401).send("Please log in.");
  }
});

// Logout route
app.post("/logout", (req, res) => {
  req.session.destroy((err) => {
    if (err) {
      return res.status(500).send("Could not log out.");
    }
    res.clearCookie("connect.sid"); // Clear the session cookie
    res.send("Logged out successfully!");
  });
});
```

### 🔑 10.3. Token-Based Authentication (JWT - JSON Web Tokens)

This is the modern, **stateless** standard for securing REST APIs. **JWT** (pronounced "jot") is a compact, URL-safe means of transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed.

#### How it works:

1.  A user logs in with a username and password to your API.
2.  If the credentials are valid, the server generates a **signed JWT**. This token contains three parts, separated by dots (`.`):
    - **Header**: Typically contains the type of token (JWT) and the signing algorithm (e.g., HMAC SHA256).
    - **Payload**: Contains "claims" (statements about an entity, usually the user, and additional data). Common claims include `iss` (issuer), `exp` (expiration time), `sub` (subject), and custom data like `userId` or `roles`.
    - **Signature**: Created by taking the encoded header, the encoded payload, and a secret key, and signing them with the specified algorithm. This signature is used by the server to verify that the token has not been tampered with.
3.  The token is sent back to the client. The client stores it (usually in local storage or a secure cookie).
4.  On all subsequent requests for protected resources, the client includes the JWT in the `Authorization` header as a **Bearer Token**.
    - `Authorization: Bearer <your_jwt_here>`
5.  The server receives the token, decodes it, and **verifies its signature** using the same secret key. If the signature is valid, the server trusts the information in the token and authenticates the user.

Because the token is signed, the server can trust its contents without needing to store anything on the server-side. This makes the system **stateless and easy to scale**, as any server instance can validate the token. The `jsonwebtoken` package is the standard for creating and verifying JWTs in Node.js.

```bash
npm install jsonwebtoken
```

```javascript
// app.js
const jwt = require("jsonwebtoken");
const express = require("express");
const app = express();
app.use(express.json()); // To parse JSON request bodies

const JWT_SECRET = process.env.JWT_SECRET || "super_secret_jwt_key"; // Load from environment variable!

// Middleware to verify JWT
const authenticateJWT = (req, res, next) => {
  const authHeader = req.headers.authorization;

  if (authHeader) {
    const token = authHeader.split(" ")[1]; // Extract the token after 'Bearer '

    jwt.verify(token, JWT_SECRET, (err, user) => {
      if (err) {
        return res.status(403).json({ message: "Forbidden: Invalid token" }); // Token is invalid or expired
      }
      req.user = user; // Attach decoded user payload to request
      next(); // Proceed to the next middleware/route handler
    });
  } else {
    res.status(401).json({ message: "Unauthorized: No token provided" });
  }
};

// Login route to generate a token
app.post("/api/login", (req, res) => {
  const { username, password } = req.body;
  // In a real application, you would verify these credentials against a database
  if (username === "admin" && password === "password123") {
    // Create a payload for the token (don't put sensitive data here)
    const userPayload = { id: 1, username: "admin", roles: ["admin", "user"] };

    // Sign the token
    const accessToken = jwt.sign(userPayload, JWT_SECRET, { expiresIn: "1h" }); // Token expires in 1 hour
    res.json({ accessToken });
  } else {
    res.status(401).json({ message: "Invalid username or password" });
  }
});

// Protected route
app.get("/api/protected", authenticateJWT, (req, res) => {
  res.json({
    message: `Welcome ${req.user.username}! You have access to protected data.`,
    user: req.user,
  });
});

// Protected route for admins only
app.get("/api/admin", authenticateJWT, (req, res) => {
  if (req.user.roles && req.user.roles.includes("admin")) {
    res.json({ message: "Welcome, Admin! This is highly sensitive data." });
  } else {
    res
      .status(403)
      .json({ message: "Forbidden: You do not have admin privileges." });
  }
});

app.listen(3000, () => console.log("Auth server listening on port 3000"));
```

💡 **Security Note**: Never store JWTs directly in the browser's Local Storage if you're concerned about XSS attacks. Consider storing them in HTTP-only cookies if CSRF protection is also in place, or use a robust client-side authentication library.

### 🤝 10.4. OAuth and Social Logins (e.g., Google, GitHub)

**OAuth 2.0** is not an authentication protocol itself; it's a protocol for **delegated authorization**. It allows a user to grant a third-party application limited access to their account on another service (e.g., Google, Facebook, GitHub), without sharing their password. This is the technology behind "Log in with Google" or "Log in with GitHub" buttons.

#### The general flow (simplified):

1.  Your application (`Client`) wants to access a user's data on a `Service Provider` (e.g., Google).
2.  Your application redirects the user's browser to the `Service Provider`'s authorization endpoint.
3.  The user logs into the `Service Provider` (if not already logged in) and is asked to grant your application specific **permissions** (scopes) to their data.
4.  If the user approves, the `Service Provider` redirects the user back to your application with a temporary **authorization code**.
5.  Your server (acting as the client in this step) exchanges this authorization code with the `Service Provider`'s token endpoint for an **access token** (and sometimes a refresh token). This exchange happens server-to-server and includes your application's client ID and client secret, keeping them secure.
6.  Your server can now use this access token to make authenticated API requests to the `Service Provider` (e.g., Google's User Info API) on behalf of the user to retrieve their profile information.
7.  Your server then creates an account for the user in your own database (if they don't exist) or logs them in, possibly generating your own JWT for your application's API.

Implementing OAuth from scratch is complex due to the various steps and security considerations. Libraries like **Passport.js** abstract away this complexity and provide "strategies" for dozens of providers (Google, Facebook, Twitter, GitHub, etc.).

```bash
npm install passport passport-google-oauth20 express-session
```

```javascript
// Minimal example using Passport.js for Google OAuth
// app.js
const express = require("express");
const passport = require("passport");
const GoogleStrategy = require("passport-google-oauth20").Strategy;
const session = require("express-session"); // Required for Passport session management

const app = express();

// Load environment variables for Google Client ID and Secret
require("dotenv").config();

// Passport session setup.
//   To support persistent login sessions, Passport needs to be able to
//   serialize users into and deserialize users out of the session.
passport.serializeUser((user, done) => {
  done(null, user.id); // Store user ID in session
});

passport.deserializeUser((id, done) => {
  // Look up user in your database by ID and return user object
  // For this example, we just return a mock user
  done(null, { id: id, name: "Mock User" });
});

// Configure Google OAuth 2.0 Strategy
passport.use(
  new GoogleStrategy(
    {
      clientID: process.env.GOOGLE_CLIENT_ID,
      clientSecret: process.env.GOOGLE_CLIENT_SECRET,
      callbackURL: "http://localhost:3000/auth/google/callback", // This must match your Google Console redirect URI
    },
    (accessToken, refreshToken, profile, done) => {
      // This function is called when a user authenticates with Google.
      // Here, you would typically find or create a user in your database
      // based on the profile information (e.g., profile.id, profile.displayName, profile.emails[0].value).
      console.log("Google Profile:", profile.displayName);
      return done(null, profile); // Pass the user profile to serializeUser
    }
  )
);

// Express session middleware (important for Passport's session)
app.use(
  session({
    secret: "your_super_secret_session_key",
    resave: false,
    saveUninitialized: false,
  })
);

// Initialize Passport and restore authentication state, if any, from the session.
app.use(passport.initialize());
app.use(passport.session());

// Google OAuth login route
app.get(
  "/auth/google",
  passport.authenticate("google", { scope: ["profile", "email"] })
);

// Google OAuth callback route
app.get(
  "/auth/google/callback",
  passport.authenticate("google", { failureRedirect: "/login-failure" }),
  (req, res) => {
    // Successful authentication, redirect home or to dashboard.
    res.redirect("/profile");
  }
);

// Routes
app.get("/login-failure", (req, res) => res.send("Login failed!"));
app.get("/profile", (req, res) => {
  if (req.isAuthenticated()) {
    // Passport function to check if user is authenticated
    res.send(`Hello, ${req.user.displayName}! You are logged in.`);
  } else {
    res.redirect("/auth/google"); // Redirect to login if not authenticated
  }
});

app.get("/logout", (req, res) => {
  req.logout((err) => {
    // Passport's logout method
    if (err) {
      return next(err);
    }
    res.redirect("/");
  });
});

app.get("/", (req, res) =>
  res.send('<a href="/auth/google">Log in with Google</a>')
);

app.listen(3000, () => console.log("OAuth server running on port 3000"));
```

💡 **Environment Variables**: For OAuth, you absolutely need to set `GOOGLE_CLIENT_ID` and `GOOGLE_CLIENT_SECRET` as environment variables.

---

## 🔒 Chapter 11: Security Best Practices

Securing your API is not an afterthought; it's a critical requirement throughout the development lifecycle.

### 11.1. Protecting Against Common Vulnerabilities (XSS, CSRF)

- **XSS (Cross-Site Scripting)**: An attack where a malicious actor injects malicious scripts into your website, which then run in other users' browsers, potentially stealing cookies, session tokens, or defacing content.

  - **Prevention**:
    - **Always validate and sanitize user input** on the server-side to remove or neutralize potentially harmful code.
    - **Output escaping**: When rendering user-provided data into HTML, always escape special HTML characters. Template engines like EJS (`<%= ... %>`) and Handlebars (`{{ ... }}`) do this by default.
    - For a REST API sending JSON, the direct risk of XSS on the backend is lower (as you're sending raw data, not HTML). However, your frontend client is responsible for safely rendering that data. Ensure your frontend framework or library properly escapes data before injecting it into the DOM.

- **CSRF (Cross-Site Request Forgery)**: An attack that tricks an authenticated user's browser into unknowingly submitting a malicious request to your server, taking advantage of the browser automatically sending cookies with requests.

  - **Prevention**: This is primarily a concern for **session-based authentication** that relies on cookies, as browsers automatically attach cookies to requests to the same domain.
  - **Stateless JWTs sent in an `Authorization` header** (e.g., `Bearer` token) are **not vulnerable** to CSRF because the token is not automatically sent by the browser.
  - For session-based applications, the standard solution is to use a library like `csurf` which generates a unique, secret token for each user session. This token must be included in non-GET requests (e.g., as a hidden field in forms or a custom HTTP header), and the server verifies its presence and validity.

### 🛡️ 11.2. Using Helmet.js

**Helmet.js** is a crucial security middleware that's incredibly easy to use. It helps secure your Express app by setting various security-related HTTP headers. These headers protect against common attacks like clickjacking, cross-site scripting (XSS), insecure connections, and others.

It's as simple as this:

```bash
npm install helmet
```

```javascript
// app.js
const express = require("express");
const helmet = require("helmet"); // Import helmet

const app = express();

app.use(helmet()); // Use Helmet middleware

// You can configure specific headers if needed:
// app.use(helmet.contentSecurityPolicy({
//   directives: {
//     defaultSrc: ["'self'"],
//     scriptSrc: ["'self'", "'unsafe-inline'"],
//     // ... other directives
//   }
// }));

app.get("/", (req, res) => {
  res.send("Hello with Helmet!");
});

app.listen(3000, () => console.log("Server with Helmet running on port 3000"));
```

✅ **Recommendation**: Always include `helmet()` in your Express applications. It provides sensible defaults that significantly enhance security with minimal effort.

### 🤫 11.3. Environment Variables for Sensitive Data (`dotenv`)

You should **NEVER hardcode sensitive information** like database passwords, API keys, JWT secrets, or third-party service credentials directly in your code. Doing so is a major security risk, especially if your code is in a public repository (e.g., GitHub).

The standard practice is to use **environment variables**. The `dotenv` package makes this easy during development by loading variables from a `.env` file into `process.env`.

1.  **Install `dotenv`**:

    ```bash
    npm install dotenv
    ```

2.  **Create a file named `.env`** in your project's root directory.

3.  **Add your secrets to this file**:

    ```
    # .env
    DATABASE_URL="mongodb://localhost:27017/my_production_app"
    JWT_SECRET="a_very_long_and_random_secret_string_CHANGE_ME_IN_PROD"
    PORT=4000
    ```

    🔥 **IMPORTANT**: Add `.env` to your `.gitignore` file so it's **never committed to version control**.

    ```
    # .gitignore
    node_modules/
    .env
    ```

4.  **In your main application file (e.g., `app.js` or `server.js`), load the variables** as early as possible:

    ```javascript
    // app.js
    require("dotenv").config(); // Load environment variables from .env file

    const express = require("express");
    const app = express();

    const dbUrl = process.env.DATABASE_URL;
    const jwtSecret = process.env.JWT_SECRET;
    const port = process.env.PORT || 3000; // Use port from .env or default to 3000

    console.log("Database URL:", dbUrl);
    console.log(
      "JWT Secret (first 10 chars):",
      jwtSecret.substring(0, 10) + "..."
    );
    console.log("App Port:", port);

    app.get("/", (req, res) => {
      res.send("Sensitive data loaded from environment variables!");
    });

    app.listen(port, () => {
      console.log(`Server running on port ${port}`);
    });
    ```

    In a production environment, you will set these environment variables directly on the hosting platform (e.g., Heroku, AWS, DigitalOcean). This is the most secure and robust way to manage sensitive configuration.

---

# Part 5: Advanced Topics and Deployment

Once you've mastered building a REST API, the next steps involve adding advanced features like real-time communication, ensuring your application is robust through testing, and finally, deploying it to a production environment where real users can access it.

---

## ⚡ Chapter 12: Real-time Communication with WebSockets

Standard HTTP has a limitation: the client always has to initiate a request. For real-time applications like chat apps, live notifications, collaborative editing tools, or gaming, you need the server to be able to "push" data to the client instantly without the client constantly polling. This is where **WebSockets** come in.

### 12.1. Introduction to WebSockets

A **WebSocket** is a communication protocol that provides a persistent, **full-duplex (two-way)** communication channel between a client and a server over a single TCP connection.

- **Persistent Connection**: Unlike HTTP, which opens and closes a connection for each request-response cycle, a WebSocket connection remains open until explicitly closed.
- **Full-Duplex**: Both the client and the server can send and receive data simultaneously at any time, without waiting for the other party.
- **Low Overhead**: Once the initial "handshake" (an HTTP request that upgrades to a WebSocket connection) is complete, data frames are much smaller than HTTP requests, leading to lower latency and higher efficiency.

This enables true real-time interaction, making them ideal for applications requiring immediate data updates. 🚀

### 💬 12.2. Using Socket.IO with Express

While you can use WebSockets directly using Node.js's built-in `ws` module, the **Socket.IO** library makes the process much simpler and more robust. It provides a reliable event-based communication layer that works on almost every platform and browser, with automatic fallbacks for environments that don't natively support WebSockets (e.g., long polling).

**Socket.IO is not a pure WebSocket implementation**; it's a library that uses WebSockets as its primary transport but adds many useful features, such as:

- Automatic re-connection support.
- Packet buffering.
- Broadcasting to all connected clients or specific "rooms".
- Multiplexing (namespaces).
- Guaranteed packet delivery.

#### Example: A Simple Chat Application

1.  **Install Socket.IO**:

    ```bash
    npm install socket.io express
    ```

2.  **Server-side (`server.js`)**:

    ```javascript
    // server.js
    const express = require("express");
    const http = require("http"); // Node.js built-in HTTP module
    const { Server } = require("socket.io"); // Import Server from socket.io

    const app = express();
    const server = http.createServer(app); // Create an HTTP server from the Express app
    const io = new Server(server); // Attach Socket.IO to the HTTP server

    // Serve a simple HTML file for the client (our chat interface)
    app.get("/", (req, res) => {
      res.sendFile(__dirname + "/public/index.html");
    });

    // Listen for new Socket.IO connections
    io.on("connection", (socket) => {
      console.log("✨ A user connected:", socket.id);

      // Listen for 'chat message' events from a client
      socket.on("chat message", (msg) => {
        console.log("Message received:", msg);
        // Broadcast the message to all connected clients
        io.emit("chat message", msg); // `io.emit` sends to all connected sockets
      });

      // Listen for 'disconnect' event when a user leaves
      socket.on("disconnect", () => {
        console.log("💔 User disconnected:", socket.id);
      });
    });

    const PORT = process.env.PORT || 3000;
    server.listen(PORT, () => {
      console.log(`Server listening on *:${PORT}`);
      console.log(`Open your browser to http://localhost:${PORT}`);
    });
    ```

3.  **Client-side (`public/index.html`)**: Create a `public` folder and an `index.html` file inside it.

    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <title>Simple Chat</title>
        <style>
          body {
            margin: 0;
            padding-bottom: 3rem;
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
              Helvetica, Arial, sans-serif;
          }
          #form {
            background: rgba(0, 0, 0, 0.15);
            padding: 0.25rem;
            position: fixed;
            bottom: 0;
            left: 0;
            right: 0;
            display: flex;
            height: 3rem;
            box-sizing: border-box;
            backdrop-filter: blur(10px);
          }
          #input {
            border: none;
            padding: 0 1rem;
            flex-grow: 1;
            border-radius: 2rem;
            margin: 0.25rem;
          }
          #input:focus {
            outline: none;
          }
          #form > button {
            background: #333;
            border: none;
            padding: 0 1rem;
            margin: 0.25rem;
            border-radius: 3px;
            outline: none;
            color: #fff;
          }
          #messages {
            list-style-type: none;
            margin: 0;
            padding: 0;
          }
          #messages > li {
            padding: 0.5rem 1rem;
          }
          #messages > li:nth-child(odd) {
            background: #efefef;
          }
        </style>
      </head>
      <body>
        <ul id="messages"></ul>
        <form id="form" action="">
          <input id="input" autocomplete="off" /><button>Send</button>
        </form>

        <script src="/socket.io/socket.io.js"></script>
        <script>
          const socket = io(); // Connect to the Socket.IO server

          const form = document.getElementById("form");
          const input = document.getElementById("input");
          const messages = document.getElementById("messages");

          // Send message when form is submitted
          form.addEventListener("submit", (e) => {
            e.preventDefault();
            if (input.value) {
              socket.emit("chat message", input.value); // Emit 'chat message' event
              input.value = "";
            }
          });

          // Listen for 'chat message' events from the server
          socket.on("chat message", (msg) => {
            const item = document.createElement("li");
            item.textContent = msg;
            messages.appendChild(item);
            window.scrollTo(0, document.body.scrollHeight);
          });
        </script>
      </body>
    </html>
    ```

    Run `node server.js` and open `http://localhost:3000` in multiple browser tabs to see the real-time chat in action\!

---

## 🧪 Chapter 13: Testing Your Application

Writing tests is essential for creating reliable, professional software. Tests verify that your code works as expected and prevent you from accidentally breaking existing features when you add new ones (this is called "**regression**").

### 13.1. Unit Testing (with Jest or Mocha/Chai)

**Unit Tests** focus on the smallest, most isolated pieces of your code—typically a single function, class method, or module. The goal is to verify that the unit works correctly on its own, without worrying about its dependencies.

**Jest** is a popular, all-in-one testing framework developed by Facebook that makes unit testing easy. It includes a test runner, assertion library, and mocking capabilities.

1.  **Install Jest**:

    ```bash
    npm install --save-dev jest
    ```

2.  **Configure `package.json`**: Add a test script.

    ```json
    "scripts": {
      "test": "jest"
    }
    ```

3.  **Example: Testing a simple utility function**

    #### `utils.js`

    ```javascript
    // utils.js
    const add = (a, b) => a + b;
    const multiply = (a, b) => a * b;
    const isEven = (num) => num % 2 === 0;

    module.exports = { add, multiply, isEven };
    ```

    #### `utils.test.js` (or `__tests__/utils.test.js`)

    ```javascript
    // utils.test.js
    const { add, multiply, isEven } = require("./utils"); // Path relative to the test file

    // 'describe' groups related tests together, providing context.
    describe("Math Utility Functions", () => {
      // 'it' or 'test' defines an individual test case.
      it("should correctly add two positive numbers", () => {
        // 'expect' creates an assertion to check if a value matches expectations.
        expect(add(2, 3)).toBe(5);
      });

      it("should handle negative numbers in addition", () => {
        expect(add(-1, 5)).toBe(4);
      });

      it("should correctly multiply two numbers", () => {
        expect(multiply(4, 5)).toBe(20);
        expect(multiply(-2, 3)).toBe(-6);
      });

      it("should return true for even numbers", () => {
        expect(isEven(2)).toBe(true);
        expect(isEven(0)).toBe(true);
      });

      it("should return false for odd numbers", () => {
        expect(isEven(3)).toBe(false);
        expect(isEven(99)).toBe(false);
      });
    });
    ```

4.  **Run tests**: `npm test`

### 🔄 13.2. Integration Testing

**Integration Tests** check how different parts of your application work together. For example, does your route handler (Controller) correctly call your business logic (Service), and does the service format the data correctly before returning it?

In these tests, you often "**mock**" external dependencies like databases or external APIs to keep the tests fast, predictable, and isolated from external system failures. Mocking means replacing a real dependency with a controlled, simulated version.

Example (conceptual):
Testing a controller that uses a service:

```javascript
// controllers/userController.js
const userService = require("../services/userService");

const getUserById = async (req, res, next) => {
  try {
    const user = await userService.findUserById(req.params.id);
    if (!user) {
      return res.status(404).json({ message: "User not found" });
    }
    res.json(user);
  } catch (error) {
    next(error);
  }
};
module.exports = { getUserById };

// services/userService.js
const User = require("../models/User"); // Mongoose model

const findUserById = async (id) => {
  return await User.findById(id); // Actual database call
};
module.exports = { findUserById };

// __tests__/userController.test.js (Integration test with mocking)
const userController = require("../controllers/userController");
const userService = require("../services/userService"); // Import the service to mock it

// Mock the userService.findUserById method
jest.mock("../services/userService"); // Automatically mocks all exports of userService

describe("userController.getUserById", () => {
  let mockReq, mockRes, mockNext;

  beforeEach(() => {
    mockReq = { params: { id: "someId" } };
    mockRes = {
      json: jest.fn(), // Mock json method
      status: jest.fn().mockReturnThis(), // Mock status and allow chaining
    };
    mockNext = jest.fn(); // Mock next function
  });

  it("should return user if found", async () => {
    const mockUser = { id: "someId", name: "Test User" };
    userService.findUserById.mockResolvedValue(mockUser); // Mock service to resolve with a user

    await userController.getUserById(mockReq, mockRes, mockNext);

    expect(userService.findUserById).toHaveBeenCalledWith("someId");
    expect(mockRes.json).toHaveBeenCalledWith(mockUser);
    expect(mockRes.status).not.toHaveBeenCalled();
    expect(mockNext).not.toHaveBeenCalled();
  });

  it("should return 404 if user not found", async () => {
    userService.findUserById.mockResolvedValue(null); // Mock service to resolve with null

    await userController.getUserById(mockReq, mockRes, mockNext);

    expect(userService.findUserById).toHaveBeenCalledWith("someId");
    expect(mockRes.status).toHaveBeenCalledWith(404);
    expect(mockRes.json).toHaveBeenCalledWith({ message: "User not found" });
    expect(mockNext).not.toHaveBeenCalled();
  });

  it("should call next with error if service throws an error", async () => {
    const serviceError = new Error("Database error");
    userService.findUserById.mockRejectedValue(serviceError); // Mock service to reject

    await userController.getUserById(mockReq, mockRes, mockNext);

    expect(userService.findUserById).toHaveBeenCalledWith("someId");
    expect(mockNext).toHaveBeenCalledWith(serviceError);
    expect(mockRes.status).not.toHaveBeenCalled(); // Error handled by global error middleware
  });
});
```

### 🎯 13.3. End-to-End Testing (with Supertest)

**End-to-End (E2E) Tests** simulate a real user's journey through your entire application stack, from the HTTP request received by your server to the database interactions and the final HTTP response. For a REST API, this means making actual HTTP requests to your endpoints and verifying that the HTTP responses (status codes, headers, and body) are correct.

The **Supertest** library is perfect for this, as it lets you programmatically make requests to your Express app without needing to run it on a live port. It wraps your Express app and allows you to test it as if it were a running server.

1.  **Install Supertest**:

    ```bash
    npm install --save-dev supertest
    ```

2.  **Example E2E test file (`api.test.js`)**:

    ```javascript
    // api.test.js
    const request = require("supertest");
    const app = require("../app"); // Your main Express app file (e.g., app.js or server.js)
    // Ensure your app.js exports the Express app instance: module.exports = app;

    // You might want to setup a test database for E2E tests,
    // or clear the database before each test suite.
    // For simplicity, this example assumes data might exist.

    describe("API Endpoints", () => {
      it("GET /api/users should respond with a 200 status code and a JSON array of users", async () => {
        // Make a GET request to /api/users
        const response = await request(app)
          .get("/api/users")
          .expect("Content-Type", /json/) // Expect Content-Type to be JSON
          .expect(200); // Expect a 200 OK status code

        // Assert that the response body is an array
        expect(response.body).toBeInstanceOf(Array);
        // Optionally, check for specific properties of users if you know their structure
        // expect(response.body[0]).toHaveProperty('id');
        // expect(response.body[0]).toHaveProperty('name');
      });

      it("POST /api/users should create a new user and respond with 201", async () => {
        const newUser = { name: "Test User", email: "test@example.com" };
        const response = await request(app)
          .post("/api/users")
          .send(newUser) // Send the request body
          .expect("Content-Type", /json/)
          .expect(201); // Expect 201 Created status

        expect(response.body).toHaveProperty("id"); // Expect the new user to have an ID
        expect(response.body.name).toBe(newUser.name);
        expect(response.body.email).toBe(newUser.email);
      });

      it("GET /api/users/:id should respond with a 404 for a non-existent user", async () => {
        await request(app)
          .get("/api/users/nonexistentid") // Request a user that surely doesn't exist
          .expect("Content-Type", /json/)
          .expect(404); // Expect 404 Not Found
      });

      // You can add more tests for PUT, DELETE, and error scenarios.
    });
    ```

    💡 **Test Database**: For E2E tests involving a database, it's highly recommended to use a separate test database or a mechanism to clean/reset the database state before each test suite to ensure tests are independent and repeatable.

---

## 📈 Chapter 14: Performance and Scalability

As your application's traffic grows, you'll need strategies to handle the increased load efficiently.

### 💨 14.1. Caching Strategies

**Caching** is the practice of storing the results of expensive operations (like database queries, API responses, or complex computations) in a temporary, high-speed data store. When the same data is requested again, it can be served from the cache instead of re-computing it or hitting the database, drastically improving response times and reducing load on your primary data sources.

A popular tool for caching in Node.js applications is **Redis**, an in-memory data store known for its speed and versatility (it can act as a cache, message broker, and more).

```bash
npm install redis
```

```javascript
// Example using Redis for simple API response caching
const express = require("express");
const redis = require("redis");
const app = express();

const REDIS_PORT = process.env.REDIS_PORT || 6379;
const client = redis.createClient(REDIS_PORT); // Connect to Redis

// Handle Redis connection errors
client.on("error", (err) => {
  console.error("Redis Client Error", err);
});

// Mock data for demonstration
const mockUserData = { id: 1, name: "Cached User", email: "cache@example.com" };

// Middleware to check cache before hitting route handler
const checkCache = (req, res, next) => {
  const { id } = req.params;

  client.get(`user_${id}`, (err, data) => {
    if (err) {
      console.error("Cache error:", err);
      return next(); // Continue if cache has an error
    }

    if (data !== null) {
      console.log("Cache hit! Serving from Redis.");
      res.json(JSON.parse(data)); // Serve from cache
    } else {
      console.log("Cache miss. Fetching from source.");
      next(); // Continue to route handler
    }
  });
};

// Route to get user by ID, with caching
app.get("/api/users/:id", checkCache, async (req, res) => {
  const { id } = req.params;
  // Simulate a database call
  console.log('Fetching user from "database"...');
  await new Promise((resolve) => setTimeout(resolve, 1000)); // Simulate delay

  // In a real app, you would fetch from DB here
  const user = { ...mockUserData, id: parseInt(id) };

  // Store data in cache (expires in 60 seconds)
  client.setex(`user_${id}`, 60, JSON.stringify(user));
  res.json(user);
});

app.listen(3000, () => {
  console.log("Server with Caching running on port 3000");
  console.log("Try visiting http://localhost:3000/api/users/1 several times.");
});
```

### ⚖️ 14.2. The `cluster` Module for Multi-Core Scaling

By default, a Node.js application runs in a **single process** on a **single CPU core**. On a modern server with multiple cores, this is inefficient as it doesn't utilize all available processing power.

The built-in **`cluster` module** allows you to easily create child processes (workers) that can run concurrently and share the same server port. Each worker runs a separate instance of your Node.js application, effectively distributing the load across multiple CPU cores, dramatically increasing the number of requests your application can handle.

```javascript
// server.js (main file for clustering)
const cluster = require("cluster");
const os = require("os"); // For getting CPU count

if (cluster.isMaster) {
  // For Node.js 16+, use cluster.isPrimary
  const numCPUs = os.cpus().length;
  console.log(`Master process ${process.pid} is running`);
  console.log(`Forking ${numCPUs} worker processes...`);

  // Fork workers for each CPU core
  for (let i = 0; i < numCPUs; i++) {
    cluster.fork();
  }

  // Listen for worker exit events
  cluster.on("exit", (worker, code, signal) => {
    console.log(
      `Worker ${worker.process.pid} died with code ${code}, signal ${signal}`
    );
    console.log("Forking a new worker...");
    cluster.fork(); // Replace the dead worker
  });

  // Optional: Handle online event
  cluster.on("online", (worker) => {
    console.log(`Worker ${worker.process.pid} is online`);
  });
} else {
  // This is a worker process, it runs the actual Express app
  const express = require("express");
  const app = express();
  const PORT = process.env.PORT || 3000;

  app.get("/", (req, res) => {
    res.send(`Hello from worker ${process.pid}!`);
  });

  app.get("/heavy", (req, res) => {
    // Simulate a CPU-intensive task
    let sum = 0;
    for (let i = 0; i < 1e9; i++) {
      sum += i;
    }
    res.send(
      `Heavy computation completed by worker ${process.pid}. Result: ${sum}`
    );
  });

  app.listen(PORT, () => {
    console.log(`Worker ${process.pid} listening on port ${PORT}`);
  });
}
```

Run `node server.js` and observe multiple worker processes starting. Requests to `/heavy` will now be distributed, preventing one slow request from blocking others.

### 🖥️ 14.3. Using a Process Manager (PM2)

When you run `node app.js` in production, what happens if your app crashes? It stays down until you manually restart it. This is unacceptable for a production application.

A **process manager** like **PM2** is essential for any production Node.js application. PM2 is a daemon (a background process) that runs your app in the background and provides crucial features for managing, monitoring, and scaling your applications.

#### Key Features of PM2:

- **Auto-Restart**: Automatically restarts your application if it crashes, ensuring high availability.
- **Clustering**: A built-in load balancer that makes it easy to run your app in cluster mode, taking full advantage of multi-core CPUs without manually using the `cluster` module.
- **Zero-Downtime Reloads**: Allows you to update your application code without any downtime for users.
- **Monitoring**: Provides tools to monitor your app's CPU, memory usage, and logs.
- **Log Management**: Centralized logging for all your application instances.

#### Basic PM2 Usage:

1.  **Install PM2 globally**:
    ```bash
    npm install -g pm2
    ```
2.  **Start your application**:
    ```bash
    pm2 start app.js # Starts your app in the background
    ```
3.  **Start in cluster mode (recommended for production)**:
    ```bash
    pm2 start app.js -i 0 # Starts one instance per CPU core
    # or pm2 start app.js -i max # Similar to -i 0, but automatically detects number of cores
    ```
4.  **List running processes**:
    ```bash
    pm2 list
    ```
5.  **Monitor processes**:
    ```bash
    pm2 monit
    ```
6.  **Stop an application**:
    ```bash
    pm2 stop app
    ```
7.  **Restart an application**:
    ```bash
    pm2 restart app
    ```
8.  **Reload for zero-downtime updates**:
    ```bash
    pm2 reload app # Reloads workers one by one without downtime
    ```
9.  **Delete an application from PM2 list**:
    ```bash
    pm2 delete app
    ```
10. **Save current process list to restart on boot**:
    ```bash
    pm2 save # Saves current running processes
    pm2 startup # Generates and configures a startup script for your OS
    ```

PM2 simplifies production deployments significantly.

---

## 🌐 Chapter 15: Deployment

Deployment is the process of taking your application from your local machine and making it accessible to the world on the internet.

### 15.1. Preparing for Production

Before deploying, ensure you:

- **Set the environment variable `NODE_ENV=production`**: This is crucial. Express, and many other Node.js libraries, use this variable to enable performance optimizations, disable development-only features (like detailed error messages), and activate stricter caching.
  - Example: `NODE_ENV=production node app.js` or configure it on your hosting platform.
- **Use environment variables for all secrets and configuration**: As discussed in Chapter 11.3, never hardcode sensitive data.
- **Implement robust logging**: Use a logging library (like Winston or Pino) to track errors, warnings, and general activity. In production, logs are your eyes and ears. Ensure logs are persisted and accessible (e.g., sent to a log management service).
- **Minimize downtime**: Consider using process managers like PM2 for auto-restarts and zero-downtime reloads.
- **Set up monitoring**: Monitor CPU, memory, network I/O, and application-specific metrics.
- **Optimize static assets**: For single-page applications, pre-build and serve static files efficiently (e.g., using a CDN or Nginx).

### 🚀 15.2. Deploying to Heroku

**Heroku** is a Platform as a Service (PaaS) that makes deployment incredibly simple, especially for Node.js applications. You just push your code to Heroku using Git, and the platform handles almost everything else: provisioning servers (dynos), installing dependencies, and running your application. It's a fantastic choice for beginners, prototypes, and small-to-medium-sized projects.

#### Basic Steps:

1.  **Install Heroku CLI**: Follow instructions on Heroku's website.
2.  **Log in**: `heroku login`
3.  **Create a `Procfile`**: In your project root, create a file named `Procfile` (no extension) to tell Heroku how to start your app.
    ```
    web: node app.js # Or whatever your main server file is
    ```
    - If using PM2: `web: pm2-runtime start app.js --no-daemon` (Requires `pm2` as a dependency).
4.  **Create a Heroku app**: `heroku create <your-app-name-optional>`
5.  **Set environment variables**:
    `heroku config:set JWT_SECRET=your_production_secret DATABASE_URL=your_db_url`
6.  **Deploy**:
    ```bash
    git add .
    git commit -m "Ready for Heroku deployment"
    git push heroku main # Or master, depending on your branch name
    ```

Heroku automatically detects your Node.js app, installs dependencies (`npm install`), and runs your `Procfile` command. Your app will be accessible at `https://<your-app-name>.herokuapp.com`.

### 🐧 15.3. Deploying to a VPS (e.g., DigitalOcean, AWS EC2) with Nginx

A **Virtual Private Server (VPS)**, such as DigitalOcean Droplets or AWS EC2 instances, gives you your own virtual server where you have full control over the environment. This approach is more flexible and powerful but requires more manual setup and system administration knowledge.

A standard practice is to use **Nginx** as a **reverse proxy** that sits in front of your Node.js application.

#### How Nginx helps:

- **Load Balancing**: If you run multiple Node.js instances (e.g., with PM2 cluster mode), Nginx can distribute incoming requests among them, improving performance and reliability.
- **SSL Termination**: Nginx can handle HTTPS encryption/decryption, offloading this CPU-intensive task from your Node.js application.
- **Serving Static Files**: Nginx is extremely efficient at serving static assets (HTML, CSS, JavaScript, images). You can configure Nginx to serve these directly, freeing up your Node.js app to focus on dynamic API requests.
- **Caching**: Nginx can also provide basic content caching.
- **Security**: Can act as a first line of defense against some attacks.

#### General Steps:

1.  **Provision a VPS**: Choose an OS (e.g., Ubuntu).
2.  **SSH into your server**:
3.  **Install Node.js and npm**: Using a Node Version Manager (NVM) is recommended.
4.  **Install PM2**: `npm install -g pm2`
5.  **Clone your repository**: `git clone <your-repo-url>`
6.  **Install dependencies**: `npm install`
7.  **Set environment variables**: Directly on the server (e.g., using a `.env` file and `dotenv` for `pm2` or by setting them in the shell).
8.  **Start your app with PM2**: `pm2 start app.js -i max --name my-api`
    - Save PM2 state: `pm2 save` and `pm2 startup` for automatic restarts.
9.  **Install Nginx**: `sudo apt update && sudo apt install nginx`
10. **Configure Nginx**: Create an Nginx server block configuration file (e.g., `/etc/nginx/sites-available/my-api`) to proxy requests to your Node.js app (which runs on a local port, e.g., 3000).

    ```nginx
    # /etc/nginx/sites-available/my-api
    server {
        listen 80;
        server_name your_domain.com www.your_domain.com; # Replace with your domain

        location / {
            proxy_pass http://localhost:3000; # Forward requests to your Node.js app
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection 'upgrade';
            proxy_set_header Host $host;
            proxy_cache_bypass $http_upgrade;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
            proxy_set_header X-Real-IP $remote_addr;
        }

        # Optional: Serve static files directly with Nginx
        # location /static/ {
        #     alias /path/to/your/app/public/;
        #     expires 30d; # Cache static files for 30 days
        # }
    }
    ```

11. **Enable Nginx config**:
    ```bash
    sudo ln -s /etc/nginx/sites-available/my-api /etc/nginx/sites-enabled/
    sudo nginx -t # Test Nginx configuration
    sudo systemctl restart nginx # Restart Nginx
    ```
12. **Configure Firewall**: Open ports 80 (HTTP) and 443 (HTTPS).
13. **Set up HTTPS (SSL/TLS)**: Use Certbot with Let's Encrypt for free SSL certificates.

### 🐳 15.4. Containerization with Docker

**Docker** is a platform for creating and running applications in **containers**. A container packages your application's code along with all its dependencies (like the Node.js runtime, specific Node.js version, system libraries, configuration files, etc.) into a single, portable, and isolated unit.

#### Benefits of Docker:

- **"Works on my machine" problem solved**: A containerized application will run identically everywhere (developer laptop, testing environment, production server), eliminating environment inconsistencies.
- **Isolation**: Containers provide process and file system isolation, preventing conflicts between applications.
- **Portability**: You can move a Docker container from one environment to another, and it will run the same way.
- **Scalability**: Easily scale applications by spinning up multiple instances of the same container.
- **Efficiency**: Containers are lightweight and share the host OS kernel, making them more efficient than traditional virtual machines.

#### Basic Docker Steps:

1.  **Install Docker Desktop** (for development) or Docker Engine (for servers).

2.  **Create a `Dockerfile`**: In your project root, define how your application image should be built.

    ```dockerfile
    # Use an official Node.js runtime as a parent image
    FROM node:18-alpine

    # Set the working directory in the container
    WORKDIR /usr/src/app

    # Copy package.json and package-lock.json to install dependencies
    COPY package*.json ./

    # Install app dependencies
    RUN npm install --production

    # Copy the rest of the application code
    COPY . .

    # Expose the port your app runs on
    EXPOSE 3000

    # Command to run the application
    CMD [ "node", "app.js" ]
    ```

3.  **Create a `.dockerignore` file**: Similar to `.gitignore`, specifies files/folders to exclude from the Docker build context.

    ```
    # .dockerignore
    node_modules
    npm-debug.log
    .env
    .git
    ```

4.  **Build the Docker image**:

    ```bash
    docker build -t my-node-app . # -t tags the image with a name
    ```

5.  **Run the Docker container**:

    ```bash
    docker run -p 80:3000 -d my-node-app # -p maps host port 80 to container port 3000, -d runs in detached mode
    ```

    Now your app is accessible on `http://localhost:80`.

For multi-service applications (e.g., Node.js API + MongoDB database), you would use **Docker Compose** to define and run them together. Docker is the modern standard for building and deploying scalable applications in cloud-native environments.

---

# 📚 Appendix

### A. Useful `npm` Packages

- [`nodemon`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/nodemon%5D(https://www.npmjs.com/package/nodemon)>): **Development Utility** - Automatically restarts your Node.js server during development when files change. Essential for rapid development.
  ```bash
  npm install -g nodemon # Global install
  nodemon app.js
  ```
- [`axios`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/axios%5D(https://www.npmjs.com/package/axios)>): **HTTP Client** - A promise-based HTTP client for making requests to other APIs or external services from your Node.js application.
  ```bash
  npm install axios
  ```
  ```javascript
  const axios = require("axios");
  async function fetchData() {
    try {
      const response = await axios.get(
        "https://jsonplaceholder.typicode.com/todos/1"
      );
      console.log(response.data);
    } catch (error) {
      console.error(error);
    }
  }
  fetchData();
  ```
- [`lodash`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/lodash%5D(https://www.npmjs.com/package/lodash)>): **Utility Library** - A library full of highly optimized utility functions for working with arrays, objects, strings, numbers, etc., making your code more concise and readable.
  ```bash
  npm install lodash
  ```
  ```javascript
  const _ = require("lodash");
  const users = [
    { user: "barney", age: 36 },
    { user: "fred", age: 40 },
  ];
  console.log(_.find(users, { age: 36 })); // { 'user': 'barney', 'age': 36 }
  ```
- [`date-fns`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/date-fns%5D(https://www.npmjs.com/package/date-fns)>) or [`day.js`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/dayjs%5D(https://www.npmjs.com/package/dayjs)>): **Date Manipulation** - Modern, lightweight libraries for parsing, formatting, validating, and manipulating dates in a more robust way than built-in JavaScript `Date` objects.
  ```bash
  npm install date-fns
  ```
  ```javascript
  const { format, addDays } = require("date-fns");
  const today = new Date();
  console.log(format(today, "yyyy-MM-dd")); // e.g., 2025-07-03
  console.log(format(addDays(today, 7), "MM/dd/yyyy")); // Date 7 days from now
  ```
- [`bcrypt`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/bcrypt%5D(https://www.npmjs.com/package/bcrypt)>): **Password Hashing** - For securely hashing passwords before storing them in your database. Crucial for security; never store plaintext passwords.
  ```bash
  npm install bcrypt
  ```
  ```javascript
  const bcrypt = require("bcrypt");
  const saltRounds = 10;
  async function hashPassword(password) {
    const hashedPassword = await bcrypt.hash(password, saltRounds);
    console.log("Hashed Password:", hashedPassword);
    const match = await bcrypt.compare(password, hashedPassword);
    console.log("Password matches:", match);
  }
  hashPassword("mysecretpassword");
  ```
- [`passport`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/passport%5D(https://www.npmjs.com/package/passport)>): **Authentication Middleware** - A comprehensive and flexible authentication middleware for Node.js. It supports various "strategies" for different authentication mechanisms (local, JWT, OAuth, etc.).
  ```bash
  npm install passport
  ```
- [`joi`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/joi%5D(https://www.npmjs.com/package/joi)>) or [`zod`](<https://www.google.com/search?q=%5Bhttps://www.npmjs.com/package/zod%5D(https://www.npmjs.com/package/zod)>): **Data Validation** - Powerful libraries for defining schemas and validating incoming data (e.g., request bodies) against those schemas. Essential for maintaining data integrity and security.
  ```bash
  npm install joi
  ```
  ```javascript
  const Joi = require("joi");
  const userSchema = Joi.object({
    username: Joi.string().alphanum().min(3).max(30).required(),
    email: Joi.string().email().required(),
    password: Joi.string()
      .pattern(new RegExp("^[a-zA-Z0-9]{3,30}$"))
      .required(),
  });
  const { error, value } = userSchema.validate({
    username: "john_doe",
    email: "john@example.com",
    password: "abc",
  });
  if (error) {
    console.log(error.details[0].message); // Password fails pattern
  } else {
    console.log("Validated data:", value);
  }
  ```

### B. Node.js and Express.js Cheat Sheet

#### `npm` Commands:

- `npm init -y`: Create a `package.json` file with default values.
- `npm install <package>`: Install a package and add it to `dependencies`.
- `npm install --save-dev <package>`: Install a package and add it to `devDependencies`.
- `npm install`: Install all dependencies listed in `package.json`.
- `npm run <script>`: Run a custom script defined in `package.json`'s `scripts` section.
- `npm start`: A common alias for `npm run start`.
- `npm test`: A common alias for `npm run test`.

#### Core Modules:

- `const fs = require('fs');`: File System module for interacting with files and directories.
- `const path = require('path');`: Path module for handling and transforming file paths (cross-platform).
- `const http = require('http');`: HTTP module for creating HTTP servers and clients.
- `const os = require('os');`: OS module for interacting with the operating system.
- `process`: Global object providing information about, and control over, the current Node.js process.

#### Express Basics:

- `const express = require('express');`
- `const app = express();`
- `app.listen(3000, () => console.log('Server running on port 3000'));`
- `app.use(express.json());`: Middleware to parse JSON request bodies.
- `app.use(express.urlencoded({ extended: true }));`: Middleware to parse URL-encoded request bodies.
- `app.use(express.static('public'));`: Middleware to serve static files from the 'public' directory.

#### Routing:

- `app.get('/path', (req, res) => { /* handler */ });`: Handles GET requests.
- `app.post('/path', (req, res) => { /* handler */ });`: Handles POST requests.
- `app.put('/path', (req, res) => { /* handler */ });`: Handles PUT requests.
- `app.delete('/path', (req, res) => { /* handler */ });`: Handles DELETE requests.
- `const router = express.Router();`: Create a modular router instance.
- `app.use('/prefix', router);`: Mount a router at a specific URL prefix.

#### Request & Response:

- `req.params.id`: Access route parameters (e.g., from `/users/:id`).
- `req.query.key`: Access query string parameters (e.g., from `/search?key=value`).
- `req.body`: Access the parsed request body (requires `express.json()` or `express.urlencoded()`).
- `req.headers`: Access HTTP request headers.
- `res.send('Hello');`: Send a basic string response.
- `res.json({ data: '...' });`: Send a JSON response.
- `res.status(404).send('Not Found');`: Set HTTP status code and send response.
- `res.sendFile(filePath);`: Send a file as the response.
- `res.render('templateName', { data });`: Render a template using the configured view engine.
- `next();`: Call the next middleware function in the stack.

### C. Debugging Techniques

- **`console.log()`**: The simplest and most common method. Strategically print out the values of variables, `req.body`, `req.params`, or messages to understand the flow of your code and identify where issues occur.

  ```javascript
  app.get("/debug-route/:id", (req, res) => {
    console.log("Incoming request for ID:", req.params.id);
    console.log("Query parameters:", req.query);
    // ... more code
    res.send("Checked logs.");
  });
  ```

- **Node.js Inspector**: Node.js has a built-in debugging client.

  - Run your app with: `node inspect app.js`. This starts a command-line debugger in your terminal. You can use commands like `c` (continue), `n` (next), `s` (step), `repl` (enter debug console).
  - **Chrome DevTools for Node.js**: For a graphical debugging interface, run your app with `node --inspect app.js`. Then, open Google Chrome, navigate to `chrome://inspect`, and click "Open dedicated DevTools for Node". This provides a full debugger similar to browser debugging, allowing you to set breakpoints, inspect variables, and step through code.

- **VS Code Debugger**: The most powerful and user-friendly option for Node.js development.

  1.  **Set Breakpoints**: Click in the gutter next to the line numbers in your code. A red dot will appear, indicating a breakpoint.
  2.  **Run with Debugger**: Go to the "Run and Debug" view in VS Code (Ctrl+Shift+D or Cmd+Shift+D).
  3.  **Create a `launch.json`**: If you don't have one, click "create a launch.json file" and select "Node.js". This creates a configuration for running your app in debug mode.
  4.  **Start Debugging**: Select the appropriate configuration (e.g., "Launch Program") and press F5 or click the green "Start Debugging" button.
  5.  **Interactive Debugging**:
      - Your application will pause when it hits a breakpoint.
      - The "Variables" panel will show the current state of all variables.
      - The "Call Stack" panel shows the sequence of function calls.
      - Use the debugger controls (step over, step into, step out, continue) to navigate through your code line by line.
      - The "Debug Console" allows you to execute JavaScript code in the current context and inspect variables.

  This interactive debugging experience is invaluable for quickly diagnosing and fixing complex issues.

---

<p align="center">
  <b>Happy coding!</b> 🚀
</p>

## 👨‍💻 About the Author

**Sajib Bhattacharjee**
MERN Stack Specialist | Full-Stack Web Developer

- 🌐 [Portfolio & Projects](https://github.com/Sajib-Bhattacharjee)
- 💼 [LinkedIn](https://www.linkedin.com/in/sajib-bhattacharjee-42682a178/)
- 📧 [Contact Me](mailto:sajibbhattacjarjee2000@gmail.com)

---

<p align="center"><i>Created with ❤️ — 2025 Edition</i></p>
