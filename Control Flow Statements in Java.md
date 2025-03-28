# **Control Flow Statements in Java**

Control flow statements determine the execution order of statements in a Java program. They help in decision-making, looping, and branching. Java provides three main types of control flow statements:

1. **Decision-Making Statements (Conditional Statements)**
2. **Looping Statements (Iteration Statements)**
3. **Jump Statements (Branching Statements)**

---

## **1. Decision-Making Statements (Conditional Statements)**  
These statements allow the program to execute different code blocks based on conditions.

### **1.1 `if` Statement**  
Executes a block of code only if the condition is `true`.

**Syntax:**  
```java
if (condition) {
    // Code to execute if condition is true
}
```

### **1.2 `if-else` Statement**  
Provides an alternative block of code if the condition is `false`.

**Syntax:**  
```java
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```

### **1.3 `if-else if-else` Statement**  
Used when multiple conditions need to be checked in sequence.

**Syntax:**  
```java
if (condition1) {
    // Code to execute if condition1 is true
} else if (condition2) {
    // Code to execute if condition2 is true
} else {
    // Code to execute if all conditions are false
}
```

### **1.4 `switch` Statement**  
Executes different blocks based on the value of an expression.

**Syntax:**  
```java
switch (expression) {
    case value1:
        // Code to execute if expression == value1
        break;
    case value2:
        // Code to execute if expression == value2
        break;
    default:
        // Code to execute if no case matches
}
```

---

## **2. Looping Statements (Iteration Statements)**  
Loops are used to execute a block of code multiple times.

### **2.1 `for` Loop**  
Executes a block of code a fixed number of times.

**Syntax:**  
```java
for (initialization; condition; update) {
    // Code to execute in each iteration
}
```

### **2.2 `while` Loop**  
Executes a block of code repeatedly as long as the condition is true.

**Syntax:**  
```java
while (condition) {
    // Code to execute in each iteration
}
```

### **2.3 `do-while` Loop**  
Ensures that the block of code is executed at least once before checking the condition.

**Syntax:**  
```java
do {
    // Code to execute in each iteration
} while (condition);
```

---

## **3. Jump Statements (Branching Statements)**  
Jump statements alter the flow of execution.

### **3.1 `break` Statement**  
Used to exit a loop or a `switch` statement.

**Example:**  
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) break;
    System.out.println(i);
}
```

### **3.2 `continue` Statement**  
Skips the current iteration and moves to the next.

**Example:**  
```java
for (int i = 1; i <= 5; i++) {
    if (i == 3) continue;
    System.out.println(i);
}
```

### **3.3 `return` Statement**  
Exits from a method and optionally returns a value.

**Example:**  
```java
public static int sum(int a, int b) {
    return a + b;
}

public static void main(String[] args) {
    int result = sum(5, 10);
    System.out.println("Sum: " + result);
}
```

---

## **Summary of Java Control Flow Statements**

| Type            | Statement  | Description |
|----------------|------------|------------|
| **Decision-Making** | `if`, `if-else`, `if-else if-else` | Executes different blocks of code based on conditions |
|  | `switch` | Executes code based on a variable’s value |
| **Looping** | `for` | Repeats code a fixed number of times |
|  | `while` | Repeats code while a condition is true |
|  | `do-while` | Executes code at least once, then checks the condition |
| **Jump** | `break` | Exits a loop or `switch` statement |
|  | `continue` | Skips the current iteration and moves to the next |
|  | `return` | Exits a method and optionally returns a value |


