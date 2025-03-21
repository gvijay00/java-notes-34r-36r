# Java Basics

## What is a Language?
A **language** is a way to communicate, either between people or between people and computers. It has two important parts:

### **1. Syntax**  
The rules that decide how to write in that language (like grammar in English or how to write code in Java)

### **2. Semantics**  
The meaning of what is written (like correct sentences in English or logical correctness in programming).

### **Simple Example:**
- **Syntax** is like traffic rules—without them, driving would be confusing.
- **Semantics** is like reaching your destination—following rules without a goal does not help.

---

## Statically vs. Dynamically Typed Languages  

### **Statically Typed Languages**  
- You must mention a variable's type when creating it.
- The type of a variable cannot change later.
- **Examples:** C, C++, Java, C#

#### **Example in Java:**
```java
int number = 10;  // Correct  
number = "hello"; // Error  
```

### **Dynamically Typed Languages**  
- You do not need to mention types.
- A variable can store different types of values at different times.
- **Examples:** JavaScript, Python

#### **Example in Python:**
```python
x = 10      # Correct  
x = "hello" # Also correct  
```

### **Simple Example:**
- **Static Typing**: Like a train—always runs on fixed tracks (fixed type).
- **Dynamic Typing**: Like a car—can go on different roads (flexible type).

---

## Why Java is Popular: The Role of JVM  
- **Compiler (`javac`)** – Converts Java code into **bytecode** (a form that computers understand).
- **JVM (Java Virtual Machine)** – Runs bytecode on any computer system by converting it into machine code.

**Key Advantage**: "Write Once, Run Anywhere" (WORA) – Java programs can run on different systems without changes.

### **Simple Example:**
- JVM is like a movie player—different devices (Windows, Mac, Linux) need different players, but the movie (bytecode) remains the same.

---

## How to Save, Compile, and Run Java Files  
1. **Save**: Create a file with a `.java` extension (e.g., `Example.java`).
2. **Compile**: Convert the source code into bytecode:
   ```bash
   javac Example.java  # Creates Example.class (bytecode)  
   ```  
3. **Run**: Use JVM to execute it:
   ```bash
   java Example  
   ```  

#### **Example Java Program:**
```java
public class Example {  
    public static void main(String[] args) {  
        System.out.println("Hello, Java!");  
    }  
}  
```
- **Save** as `Example.java` → **Compile** → **Run** → **Output:** `Hello, Java!`

---  

## Bytecode and Execution Process  
**Bytecode** is the intermediate step between Java code and machine code.  
- Java code is converted into **bytecode** (`.class` files).
- The **JVM** translates bytecode into machine-specific code.
- **Advantage:** Java works on multiple systems without modification.

### **Simple Example:**
- Bytecode is like a universal script—translators (JVM) convert it into different languages (machine code) for different computers.

---  

## Compiler vs. Interpreter  

| **Feature** | **Compiler** | **Interpreter** |  
|------------|-------------|---------------|  
| **Translation** | Translates all code at once. | Translates code line by line. |  
| **Output** | Creates bytecode (`.class` file). | Directly runs the program. |  
| **Speed** | Faster because it is pre-translated. | Slower because it translates while running. |  
| **Error Checking** | Finds all errors at once. | Stops at the first error. |  
| **Platform** | Output may be platform-specific. | Works on different platforms if an interpreter exists. |

### **How Java Uses Both**  
1. **Compiler (`javac`)** – Converts `.java` to `.class` (bytecode).
2. **Interpreter (JVM)** – Reads bytecode and runs it line by line.
3. **JIT (Just-In-Time) Compilation** – Speeds up execution by converting frequently used code into machine code.

### **Simple Example:**
- JVM’s **JIT Compiler** is like a restaurant—prepares popular dishes in advance for faster service.

---  

## First Java Program: "Hello, Java!"  
The first Java program is usually **"Hello, Java!"** to help beginners understand the basics.

### **Java Code Example**
```java
public class HelloJava {
    public static void main(String[] args) {
        System.out.println("Hello, Java!");
    }
}
```

### **Explanation**
1. **Class Declaration (`public class HelloJava`)**  
   - Defines a class named `HelloJava`.
   - Every Java program has at least one class.
2. **Main Method (`public static void main(String[] args)`)**  
   - **Starting point** of every Java program.
   - `public` → Can be used from anywhere.
   - `static` → Runs without creating an object.
   - `void` → Does not return anything.
   - `main` → Special method where execution starts.
   - `String[] args` → Stores command-line arguments.
3. **Printing to Console (`System.out.println("Hello, Java!");`)**  
   - `System.out` → Standard output stream.
   - `println` → Prints text and moves to a new line.

### **How to Run the Program**
1. **Save** as `HelloJava.java`.
2. **Compile**:
   ```bash
   javac HelloJava.java
   ```
3. **Run**:
   ```bash
   java HelloJava
   ```
   **Output:** `Hello, Java!`



