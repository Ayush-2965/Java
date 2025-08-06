# Java and Web Technologies Notes

## Java Development Tools

Java has powerful development tools such as Eclipse SDK and JetBrains IDEs.  
Java is a mature language, making it stable and predictable.

**Popular IDEs:**
- JetBrains (IntelliJ IDEA)
- Eclipse

---

## J2EE Overview

J2EE (Java 2 Platform, Enterprise Edition) is a platform-independent, Java-centric environment for developing, building, and deploying web-based enterprise applications. The J2EE platform consists of a set of services and application programming interfaces (APIs).

### Enterprise Programming

Enterprise programming is a method of developing applications that help organizations manage various business activities.

---

## Advantages of J2EE

- **Platform Independence:**  
    Java provides a programming model that works consistently across the enterprise.

- **Managed Objects:**  
    J2EE offers a managed environment for components. J2EE applications are container-centric.

- **Reusability & Modularity:**  
    Code can be reused and organized into modules.

---

## Software Application Layers

Software applications can be broken into three logical layers:

1. **Presentation Layer**
2. **Business Rules Layer**
3. **Data Access Layer**

---

## Client-Server Architecture

### Client

A client is a computer that accepts data from the user and sends requests to the server for processing.

### Server

A server is a computer that processes requests from clients and sends necessary responses back. Based on the nature of requests and responses, client-server architecture can be classified as follows:

#### Single-Tier Architecture

- **Description:**  
    Client machines (dumb terminals) have no processing power; they only display what the server sends.  
    *Example:* Set-top box provides signals to the TV, which displays the video.

- **Advantages:**  
    1. Easy to implement  
    2. Low cost

- **Disadvantages:**  
    - If the server crashes, the architecture fails and all data is lost.

#### 2-Tier Architecture

- **Description:**  
    Client machines (PC terminals) have processing power.

- **Advantages:**  
    1. Clients can share the load and perform basic checks, making it faster than single-tier.

- **Disadvantages:**  
    - If the server crashes, the architecture fails and all data is lost.

#### 3-Tier Architecture

- **Description:**  
    The server part is split into two:
    1. **Web Server:** Handles client requests and responses.
    2. **Database Server:** Stores and manipulates data.

- **Advantages:**  
    1. Faster and more secure  
    2. Data security (if the web server fails, data can still be retrieved from the database server)

- **Disadvantages:**  
    1. Costly  
    2. Still a chance of data loss

#### N-Tier Architecture

- **Description:**  
    Multiple parallel servers (proxy servers) are connected to each other.

- **Advantages:**  
    1. Data loss and architecture crash are almost negligible.

- **Disadvantages:**  
    1. Costly  
    2. High complexity

---

## HTML Concepts

- **Hypertext:**  
    HTML is called hypertext because it supports hyperlinks, allowing navigation between web pages.

- **Marquee Tag:**  
    Used to move content. Attributes include `direction`, `behavior`, and `scrollamount`.

- **Lists:**  
    - `ol` (ordered list): Attributes include `type` (1, a, A, I, etc.), `start` (starting number).
    - `ul` (unordered list): Attributes include `type` (circle, disc, square).
    - Both wrap `li` (list item) elements.

- **Hyperlink:**  
    Mechanism to switch from one web page to another.

- **Frames:**  
    Allows viewing multiple web pages within a single page using the `<frameset>` tag.  
    Note: `<frameset>` does not use a `<body>` tag.

---

## HTML Forms

A form in HTML is used to accept data from the user and send requests to the server.  
Created using the `<form>` tag, which has two main attributes:

1. **method:** Determines how requests are sent (`get` or `post`).
2. **action:** Specifies which server-side code will handle the request.
## JavaScript

JavaScript is a scripting language used primarily for client-side validation of data. JavaScript code is typically written within HTML using the `<script>` tag, which is usually placed inside the `<head>` section of an HTML document.

### Compiler vs Interpreter

- **Compiler:**  
    Checks for syntax errors in the entire code before execution.

- **Interpreter:**  
    Executes code line by line.

### Working with HTML Forms in JavaScript

- In JavaScript, every HTML page is represented as a `document`.
- To access specific HTML elements, use the `document` object and its properties (e.g., `document.forms`).
- When the submit button of a form is clicked, the `onsubmit` attribute of the `<form>` tag is triggered.
- The value of the `onsubmit` attribute should be the name of the JavaScript function to be called.
- To prevent form data from being sent to the server, the function should return `false`.
- The `focus()` method is used to move the cursor to a specific textbox or input field in the form.

The `length` attribute in JavaScript is used to count the total number of characters in a textbox.
