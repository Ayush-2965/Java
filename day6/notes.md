
## Project

A project may be defined as any type of task which is implemented using the tools and technology that we have learned.

### Software Development Life Cycle (SDLC)

1. **Analysis Phase**  
    Understand the requirements and gather information about what needs to be built.

2. **Design Phase**  
    Create models such as DFD (Data Flow Diagram) and ER (Entity Relationship) diagrams to plan the system.

3. **Coding**  
    Write the actual code to implement the design.

4. **Testing Phase**  
    - **Unit Testing:** Test individual components.
    - **Integration Testing:** Test combined parts of the application.
    - **Blackbox Testing:** Test without looking at internal code structure.
    - **Whitebox Testing:** Test with knowledge of the internal code.

5. **Implementation Phase**  
    Deploy the application to the production environment.

6. **Maintenance Phase**  
    Fix bugs and update the system as needed after deployment.

---

### DFD - Data Flow Diagram

A DFD shows how data moves from its source to its destination. It uses specific symbols to represent processes, data stores, data flow, and external entities.

#### Types of DFD

- **0 Level DFD (Context Level Diagram):**  
  Shows the system as a single process with its relationships to external entities. Data store symbols are not used.

- **1st Level DFD:**  
  Breaks down the main process into sub-processes and shows data flow between them.

- **2nd Level, 3rd Level, etc.:**  
  Further decomposes processes for more detail.

---

### ER Diagram (Entity Relationship Diagram)

An ER diagram is used to determine the relationships between two or more entities in a system. It also helps in designing the database schema by identifying tables and their columns.

#### Types of Relationships

1. **One to One**
2. **One to Many**
3. **Many to One**
4. **Many to Many**

---

## MVC (Model View Controller)

MVC is an architectural pattern used to separate the application into three main components:

- **Model:** Handles data and business logic.
- **View:** Manages the display and user interface.
- **Controller:** Handles user input and updates the model and view.

This separation makes the project more secure, maintainable, and scalable.

---

### Bean

A **Bean** (also called a [POJO](https://en.wikipedia.org/wiki/Plain_old_Java_object) - Plain Old Java Object) is a Java class used to implement business logic. In a bean:

- All variables should be declared as `private`.
- Getter methods are used to retrieve values.
- Setter methods are used to set values.
- Additional methods can be added to implement business logic.

#### Steps to Create a Bean

1. Create a Java package.
2. Inside the package, create a Java class.
3. Declare variables as `private`.
4. Provide public getter and setter methods.
5. Add business logic methods as needed.

Example:

```java
package com.example.model;

public class UserBean {
     private String name;
     private int age;

     // Getter
     public String getName() {
          return name;
     }

     // Setter
     public void setName(String name) {
          this.name = name;
     }

     // Business logic method
     public boolean isAdult() {
          return age >= 18;
     }
}
```
