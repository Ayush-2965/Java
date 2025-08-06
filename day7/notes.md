
# Struts Framework Notes

Struts is an open source framework that extends the Java Servlet API and employs a Model-View-Controller (MVC) architecture. It enables us to create maintainable, extensible, and flexible web applications.

## Key Concepts

- **All client requests** are handled by the ActionServlet.
- In Struts, the "bean" is implemented using two classes:
    1. **ActionForm**: Holds form data (private variables with getters and setters).
    2. **Action**: Contains business logic in the `execute` method.

Both ActionForm and Action beans are configured in an XML file called `struts-config.xml`.

## Struts-config.xml

- Maps form beans and action classes.
- Configures navigation rules and forwards.
- Associates JSP pages with actions.

## Workflow

1. **Client Request**: User submits a form or clicks a link.
2. **ActionServlet**: Receives the request and looks up the mapping in `struts-config.xml`.
3. **ActionForm**: Populates form bean with request data.
4. **Action**: Executes business logic in the `execute` method.
5. **Forward**: Returns a logical name, which is mapped to a JSP page in `struts-config.xml`.
6. **JSP Response**: The response is sent back to the client using JSP pages.

## View Layer

- JSP pages are used to send responses back to the client.
- JSPs should be placed in the `WEB-INF` folder for security.
- JSPs must be configured in `struts-config.xml` using `<forward>` tags.

### Tag Libraries

To use Struts tags in JSP, add the following at the top of your JSP file:

```jsp
<%@ taglib uri="http://struts.apache.org/tags-html" prefix="html" %>
<%@ taglib uri="http://struts.apache.org/tags-bean" prefix="bean" %>
<%@ taglib uri="http://struts.apache.org/tags-logic" prefix="logic" %>
```

## Steps to Add the View Part in Struts

1. Create JSP pages for responses.
2. Place all response JSP pages in the `WEB-INF` folder.
3. Configure the JSP pages in `struts-config.xml` using `<forward>` elements.
4. Use Struts tag libraries in JSP for form handling and data display.

## Linking JSP Pages with Responses

- Define forwards in the action mapping in `struts-config.xml`:

```xml
<action path="/login" type="com.example.LoginAction" name="loginForm" scope="request" validate="true" input="/login.jsp">
        <forward name="success" path="/welcome.jsp"/>
        <forward name="failure" path="/login.jsp"/>
</action>
```

## Adding a Column to a Table

Syntax for adding a column in a table:

```sql
ALTER TABLE tablename ADD column_name datatype;
```

---

**Summary:**  
Struts provides a structured way to build Java web applications using MVC. It separates concerns, making code more maintainable and scalable. Configuration is primarily done in `struts-config.xml`, and JSPs are used for the view layer, enhanced by Struts tag libraries.

