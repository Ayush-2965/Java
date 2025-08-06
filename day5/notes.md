## JSP

JSP stands for Java Server Pages. Like servlets, JSP is a server-side technology used to handle requests coming from the client. In JSP, we merge code with design to create dynamic web applications. JSP supports all HTML tags, and in addition, it has its own embedded tags:

- **Directives** — page, include, taglib  
    Directives are used to instruct the JSP engine about the overall structure of the page. There are three main types:
    - **Page directive** — Used to import Java packages into the JSP page.  
        Example: `<%@ page import="java.io.*" %>`
    - **Include directive** — Used to include another file in the JSP page.  
        Example: `<%@ include file="filename.ext" %>`
    - **Taglib directive** — Required when using custom tags in the JSP page.  
        Example: `<%@ taglib uri="" %>` (where `uri` is the path)

- **Scriptlets**  
    Scriptlets allow you to write Java code within the JSP page.  
    Example: `<% java code %>`

- **Expression tag**  
    Used to display the value of an expression in the JSP page.  
    Example: `<%= s1 + s2 %>`

- **Action tags**  
    Action tags perform actions at runtime. Two common types are:
    - **Include** — Includes another JSP page at runtime.  
        Example: `<jsp:include page="filename.ext"/>`
    - **Forward** — Forwards the request to another JSP page at runtime.  
        Example: `<jsp:forward page="filename.ext"/>`

- **Declaration tag**  
    Used to declare global variables in JSP.  
    Example: `<%! int a = 10; %>`

## Implicit objects in JSP

JSP provides several built-in (implicit) objects that can be used directly:

- **request**  
    Handles the request coming from the client.
- **response**  
    Handles all types of responses sent to the client.
- **session**  
    Manages session handling in JSP.
- **out**  
    Used to display output in JSP.
- **application**  
    Used for sharing data between different components of the application.