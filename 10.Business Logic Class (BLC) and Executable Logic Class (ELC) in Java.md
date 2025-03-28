# Business Logic Class (BLC) and Executable Logic Class (ELC) in Java

In Java, **BLC (Business Logic Class)** and **ELC (Executable Logic Class)** are design concepts that separate concerns in an application, ensuring maintainability and scalability.

---

# **1. Business Logic Class (BLC)**
The **BLC** is responsible for handling business rules, calculations, and validations. It is independent of the presentation or execution layer and does not contain UI-related logic.

### **Key Responsibilities:**
- Encapsulates business rules and domain logic.
- Ensures reusability and testability.
- Can interact with databases through DAO (Data Access Object) but does not handle direct execution.

### **Example: Circle Calculation**
```java
// Business Logic Class (BLC)
public class Circle {
    private double radius;

    public Circle(double radius) {
        this.radius = radius;
    }

    public double calculateArea() {
        return Math.PI * radius * radius;
    }

    public double calculateCircumference() {
        return 2 * Math.PI * radius;
    }

    public void displayCircleDetails() {
        System.out.println("Circle Radius: " + radius);
        System.out.println("Circle Area: " + calculateArea());
        System.out.println("Circle Circumference: " + calculateCircumference());
    }
}
```

---

# **2. Executable Logic Class (ELC)**
The **ELC** acts as a controller or execution class that interacts with the user and invokes methods of the **BLC**.

### **Key Responsibilities:**
- Handles user input and output.
- Calls the BLC methods and displays results.
- Acts as a bridge between UI and business logic.
- Typically contains the `main()` method for execution.

### **Example: Circle Calculation Execution**
```java
// Executable Logic Class (ELC)
import java.util.Scanner;

public class CircleApp {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter the radius of the circle: ");
        double radius = scanner.nextDouble();

        Circle circle = new Circle(radius);
        circle.displayCircleDetails();

        scanner.close();
    }
}
```

---

## Key Differences:

| Feature             | Business Logic Class (BLC)       | Executable Logic Class (ELC) |
|--------------------|--------------------------------|-----------------------------|
| **Purpose**       | Contains business rules and logic. | Handles user interaction and execution flow. |
| **Independence**  | Independent of UI and execution logic. | Depends on BLC for processing data. |
| **Reusability**   | Can be reused in different applications. | Not reusable, specific to execution. |
| **Contains `main()`?** | No | Yes |

---

## **Why Use This Approach?**
✔ **Separation of Concerns** – BLC focuses on logic, ELC handles execution.  
✔ **Reusability** – `Circle` class can be used in different applications.  
✔ **Maintainability** – If logic changes, update only BLC.  
✔ **Testability** – `Circle` class can be tested independently without modifying the UI.  

This separation is commonly used in **MVC (Model-View-Controller)** architecture:
- **Model (BLC)** represents data and business logic.
- **View** handles UI.
- **Controller (ELC)** manages execution and user interaction.


