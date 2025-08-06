# Java Full Stack Development Repository

This repository contains a comprehensive Java Full Stack development course covering **frontend web technologies** and **Java backend** development. It demonstrates the complete journey from basic HTML/CSS/JavaScript to advanced Java web frameworks and enterprise application development.

## 📋 Table of Contents

- [Course Overview](#course-overview)
- [Technologies Covered](#technologies-covered)
- [Course Structure](#course-structure)
- [Day-by-Day Learning Path](#day-by-day-learning-path)
- [Project Examples](#project-examples)
- [Setup Instructions](#setup-instructions)
- [Key Concepts](#key-concepts)
- [Architecture Patterns](#architecture-patterns)

## 🎯 Course Overview

This repository contains a structured 7-day learning program covering full stack development with Java backend. The course progresses from fundamental web technologies to advanced enterprise frameworks, providing hands-on examples and practical implementations.

## 🛠 Technologies Covered

### Frontend Technologies
- **HTML5** - Structure and semantic markup
- **CSS3** - Styling and layouts
- **JavaScript** - Client-side scripting and validation
- **Forms & Validation** - User input handling and regex patterns

### Backend Technologies
- **Java** - Core programming language
- **J2EE/JEE** - Enterprise Java platform
- **Servlets** - Server-side request handling
- **JSP** - Java Server Pages for dynamic content
- **JDBC** - Database connectivity
- **Struts Framework** - MVC web application framework

### Database
- **RDBMS concepts** - Relational database management
- **SQL** - Database queries and operations
- **Oracle Database** - Enterprise database system

### Architecture & Design
- **3-Tier Architecture** - Presentation, Business, Data layers
- **MVC Pattern** - Model-View-Controller design
- **Session Management** - Stateful web applications
- **SDLC** - Software Development Life Cycle

## 📚 Course Structure

```
Java/
├── day1/           # HTML, Client-Server Architecture, Forms
├── day2/           # JavaScript Validation, Database Concepts, JDBC
├── day3/           # Servlets, HTTP Protocol, Request Processing
├── day4/           # Session Management, Cookies, HTTP Sessions
├── day5/           # JSP, Server Pages, Dynamic Content
├── day6/           # Project Development, MVC, Beans, SDLC
├── day7/           # Struts Framework, Enterprise Applications
└── examples/       # Practical implementations and demos
```

## 🗓 Day-by-Day Learning Path

### Day 1: Web Fundamentals & Architecture
**Topics Covered:**
- Java Development Environment (IDEs: Eclipse, IntelliJ IDEA)
- J2EE Platform Overview and Enterprise Programming
- Client-Server Architecture (Single-tier, 2-tier, 3-tier, N-tier)
- HTML Fundamentals: Forms, Tables, Lists, Hyperlinks
- Framesets and Multi-page layouts

**Practical Examples:**
- Basic HTML pages with navigation
- Restaurant menu website
- Form creation and structure
- Frameset implementations
- Sports website with hyperlinks

**Key Files:**
- `day1/index.html` - Basic HTML structure and styling
- `day1/restaurant.html` - Menu display with lists
- `day1/form/index.html` - Form validation basics
- `day1/frameset/` - Multi-frame layouts
- `day1/hyperlink/` - Navigation between pages

### Day 2: JavaScript & Database Integration
**Topics Covered:**
- JavaScript for client-side validation
- Database concepts: DBMS vs RDBMS
- Primary Keys, Foreign Keys, Unique Keys
- JDBC (Java Database Connectivity)
- Regular Expressions for validation
- Oracle Database configuration

**Practical Examples:**
- Email validation with regex patterns
- Password strength validation
- Number range validation
- Database connection setup

**Key Files:**
- `day2/emailValidation/index.html` - Email regex validation
- `day2/passwordValidation/index.html` - Password confirmation
- `day2/numberValidation/index.html` - Numeric range validation
- `day2/notes.md` - Database and JDBC concepts

**Regex Patterns Covered:**
```javascript
// Email validation
var format=/^[\w+-.]+@[\w-.]+\.[\w{2,3}]+$/;
```

### Day 3: Servlets & Server-Side Programming
**Topics Covered:**
- Servlet lifecycle (init(), service(), destroy())
- GenericServlet vs HttpServlet
- HTTP methods (GET, POST)
- Request processing and response generation
- Servlet configuration and mapping

**Practical Examples:**
- User form processing servlet
- HTTP request handling
- Data extraction from forms
- Response generation

**Key Concepts:**
```java
@WebServlet("/submit")
public class UserFormServlet extends HttpServlet {
    protected void doPost(HttpServletRequest request, 
                         HttpServletResponse response) {
        // Process form data
    }
}
```

### Day 4: Session Management
**Topics Covered:**
- Stateless vs Stateful protocols
- Session management techniques:
  - Cookies
  - HTTP Sessions
  - URL Rewriting
  - Hidden Field Format
- GET vs POST requests
- Security considerations

**Key Implementation:**
- Cookie creation and management
- Session tracking across requests
- Data persistence between pages
- Security best practices

### Day 5: JSP (Java Server Pages)
**Topics Covered:**
- JSP architecture and lifecycle
- JSP elements:
  - Directives (page, include, taglib)
  - Scriptlets `<% %>`
  - Expression tags `<%= %>`
  - Declaration tags `<%! %>`
  - Action tags (`jsp:include`, `jsp:forward`)
- Implicit objects (request, response, session, out, application)

**JSP Examples:**
```jsp
<%@ page import="java.io.*" %>
<% String name = request.getParameter("name"); %>
<%= "Hello " + name %>
```

### Day 6: Project Development & Design Patterns
**Topics Covered:**
- Software Development Life Cycle (SDLC)
- Analysis, Design, Coding, Testing, Implementation, Maintenance
- Data Flow Diagrams (DFD)
- Entity Relationship Diagrams (ERD)
- MVC Architecture pattern
- JavaBeans (POJO) development
- Project planning and execution

**Design Patterns:**
- Model: Data and business logic
- View: User interface and presentation
- Controller: Request handling and flow control

**Bean Structure:**
```java
public class UserBean {
    private String name;
    private int age;
    
    // Getters and setters
    public String getName() { return name; }
    public void setName(String name) { this.name = name; }
    
    // Business logic
    public boolean isAdult() { return age >= 18; }
}
```

### Day 7: Struts Framework
**Topics Covered:**
- Struts MVC framework
- ActionServlet and request handling
- ActionForm and Action classes
- struts-config.xml configuration
- JSP integration with Struts
- Tag libraries for view layer

**Struts Workflow:**
1. Client Request → ActionServlet
2. ActionServlet → struts-config.xml lookup
3. ActionForm → Data population
4. Action → Business logic execution
5. Forward → JSP response

**Configuration Example:**
```xml
<action path="/login" 
        type="com.example.LoginAction" 
        name="loginForm">
    <forward name="success" path="/welcome.jsp"/>
    <forward name="failure" path="/login.jsp"/>
</action>
```

## 🏗 Project Examples

### 1. Restaurant Website
- **Location:** `day1/restaurant.html`
- **Features:** Menu display, navigation, HTML lists
- **Technologies:** HTML, CSS

### 2. Form Validation System
- **Location:** `day1/form/`, `day2/emailValidation/`, `day2/passwordValidation/`
- **Features:** Client-side validation, regex patterns, user feedback
- **Technologies:** HTML, JavaScript, Regex

### 3. Sports Information Portal
- **Location:** `day1/hyperlink/`
- **Features:** Multi-page navigation, frameset layout
- **Technologies:** HTML, Framesets

### 4. User Registration System
- **Location:** `day3/notes.md` (Servlet example)
- **Features:** Form processing, data validation, response generation
- **Technologies:** Java Servlets, HTML Forms

## 🚀 Setup Instructions

### Prerequisites
- Java Development Kit (JDK) 8+
- IDE (Eclipse, IntelliJ IDEA, or NetBeans)
- Web Server (Apache Tomcat)
- Database (Oracle, MySQL)

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd fsp/Java
   ```

2. **Setup Java Environment:**
   - Install JDK
   - Configure JAVA_HOME environment variable
   - Setup IDE of choice

3. **Database Configuration:**
   ```java
   // Oracle JDBC connection
   Connection con = DriverManager.getConnection(
       "jdbc:oracle:thin:@localhost:1521:xe", 
       "username", "password"
   );
   ```

4. **Web Server Setup:**
   - Install Apache Tomcat
   - Deploy web applications
   - Configure servlet mappings

5. **Run Examples:**
   - Open HTML files in browser for frontend examples
   - Deploy servlet examples to Tomcat
   - Test database connectivity

## 🔑 Key Concepts

#### MVC Pattern
- **Model:** JavaBeans, Data Objects
- **View:** JSP pages, HTML
- **Controller:** Servlets, Struts Actions

### Session Management Comparison

| Method | Storage Location | Security | Complexity | Best Use Case |
|--------|------------------|----------|------------|---------------|
| Cookies | Client-side | Low | Low | Simple preferences |
| HTTP Session | Server-side | High | Medium | User authentication |
| URL Rewriting | URL parameters | Medium | High | Stateless applications |
| Hidden Fields | Form data | Low | Medium | Single-page workflows |

### Database Relationships

#### Key Types
- **Primary Key:** Unique identifier, no NULL values
- **Foreign Key:** References primary key of another table
- **Unique Key:** Unique values, allows NULL

#### Relationship Types
1. **One-to-One:** User ↔ Profile
2. **One-to-Many:** Customer → Orders
3. **Many-to-One:** Orders ← Customer
4. **Many-to-Many:** Students ↔ Courses

## 📖 Additional Resources

### Documentation Links
- [Oracle Java Documentation](https://docs.oracle.com/en/java/)
- [Apache Tomcat Documentation](https://tomcat.apache.org/tomcat-9.0-doc/)
- [Struts Framework Guide](https://struts.apache.org/)

### Development Tools
- **IDEs:** Eclipse, IntelliJ IDEA, NetBeans
- **Servers:** Apache Tomcat, JBoss, WebLogic
- **Databases:** Oracle, MySQL, PostgreSQL
- **Version Control:** Git, SVN

### Learning Path
1. Master HTML/CSS/JavaScript fundamentals
2. Understand database concepts and SQL
3. Learn Java servlet programming
4. Implement session management
5. Create dynamic content with JSP
6. Apply MVC patterns and design principles
7. Build enterprise applications with frameworks

## 🤝 Contributing

1. Fork the repository
2. Create feature branches
3. Follow coding standards
4. Add comprehensive documentation
5. Submit pull requests

## 📜 License

This educational repository is provided for learning purposes. Please respect intellectual property rights and use responsibly.
