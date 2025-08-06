# Servlet Notes

A **Servlet** is a server-side Java program that accepts data from clients, processes it, and sends a response back to the client.

---

## Servlet Lifecycle

The lifecycle of a servlet consists of the following main methods:

1. **init()**
    - Called once when the servlet is first loaded into memory.
    - Used for initialization tasks.

2. **service()**
    - Called for each request.
    - Processes client requests and generates responses.

3. **destroy()**
    - Called once when the servlet is being removed from memory.
    - Used for cleanup activities.

---

## Types of Servlets

### GenericServlet

- Defined in the package: `javax.servlet`
- Does **not** support HTTP protocol directly.
- Lifecycle methods: `init()`, `service()`, `destroy()`

### HttpServlet

- Defined in the package: `javax.servlet.http`
- Extends `GenericServlet` and adds support for HTTP-specific methods.
- Lifecycle methods:
    - `init()`
    - `service()` (internally calls `doGet()`, `doPost()`, etc.)
    - `destroy()`

---

## Servlet Lifecycle (HTTP)

With `HttpServlet`, the lifecycle is:

1. **init()**
2. **service()** (delegates to `doGet()`, `doPost()`, etc. based on HTTP request type)
3. **destroy()**

---

## Example: HTML Form for Servlet

Below is an example of an HTML form that can be used to collect user data and send it to a servlet:

```html
<form action="/submit" method="post">
  <label for="email">Email ID:</label>
  <input type="email" id="email" name="email" required><br>

  <label for="password">Password:</label>
  <input type="password" id="password" name="password" required><br>

  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required><br>

  <label for="contact">Contact Number:</label>
  <input type="tel" id="contact" name="contact" required><br>

  <label for="address">Address:</label>
  <input type="text" id="address" name="address" required><br>

  <label for="security-question">Security Question:</label>
  <input type="text" id="security-question" name="security-question" required><br>

  <label for="security-answer">Security Answer:</label>
  <input type="text" id="security-answer" name="security-answer" required><br>

  <button type="submit">Submit</button>
</form>
```

---

## Example: Simple Servlet Code

Below is an example of a simple servlet that processes form data submitted to the `/submit` endpoint:

**Servlet Name:** `UserFormServlet`  
**Mapped URL (action):** `/submit`  
**File Name:** `UserFormServlet.java`  
**Location:** `src/main/java/com/example/servlets/UserFormServlet.java`

```java
package com.example.servlets;

import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

@WebServlet("/submit")
public class UserFormServlet extends HttpServlet {
    @Override
    protected void doPost(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        String email = request.getParameter("email");
        String password = request.getParameter("password");
        String name = request.getParameter("name");
        String contact = request.getParameter("contact");
        String address = request.getParameter("address");
        String securityQuestion = request.getParameter("security-question");
        String securityAnswer = request.getParameter("security-answer");

        response.setContentType("text/html");
        response.getWriter().println("<h2>Form Data Received</h2>");
        response.getWriter().println("<p>Email: " + email + "</p>");
        response.getWriter().println("<p>Name: " + name + "</p>");
        // For security, do not display password in real applications
        response.getWriter().println("<p>Contact: " + contact + "</p>");
        response.getWriter().println("<p>Address: " + address + "</p>");
        response.getWriter().println("<p>Security Question: " + securityQuestion + "</p>");
        response.getWriter().println("<p>Security Answer: " + securityAnswer + "</p>");
    }
}
```

## How HTML Form and Servlet Connect

The connection between the HTML form and the servlet can be established in two ways:

### Method 1: Using @WebServlet Annotation

- The HTML form uses `action="/submit"`, which means when the form is submitted, the browser sends a POST request to the `/submit` URL.
- The servlet `UserFormServlet` is annotated with `@WebServlet("/submit")`, which tells the servlet container to map requests to `/submit` to this servlet.
- When the form is submitted, the servlet container (like Tomcat) receives the request at `/submit` and invokes the `doPost()` method of `UserFormServlet`.

### Method 2: Using web.xml Configuration (NetBeans IDE Approach)

In NetBeans IDE, you can configure servlet mappings through the `web.xml` file instead of using annotations:

**web.xml Configuration:**
```xml
<servlet>
    <servlet-name>UserFormServlet</servlet-name>
    <servlet-class>com.example.servlets.UserFormServlet</servlet-class>
</servlet>

<servlet-mapping>
    <servlet-name>UserFormServlet</servlet-name>
    <url-pattern>/UserFormServlet</url-pattern>
</servlet-mapping>
```

**HTML Form (NetBeans approach):**
```html
<form action="UserFormServlet" method="post">
  <!-- form fields remain the same -->
</form>
```

**Servlet Code (without @WebServlet annotation):**
```java
package com.example.servlets;

import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

public class UserFormServlet extends HttpServlet {
    @Override
    protected void doPost(HttpServletRequest request, HttpServletResponse response)
            throws ServletException, IOException {
        // servlet logic remains the same
    }
}
```

### Key Differences:

- **@WebServlet Annotation:** Direct mapping in the servlet class itself
- **web.xml Configuration:** Centralized configuration, commonly used in NetBeans IDE
- **Action Attribute:** Can directly reference the servlet class name when using web.xml mapping

**Summary:**  
In NetBeans IDE, you typically use `web.xml` for servlet configuration and can directly set the servlet class name in the form's action attribute, eliminating the need for `@WebServlet` annotations.

