# Non-Static Methods in Java

## Introduction
In Java, methods can be classified as **static** or **non-static**. Non-static methods, also known as **instance methods**, belong to objects of a class rather than the class itself. These methods require an instance of the class to be invoked.

## Characteristics of Non-Static Methods
1. **Instance-Specific**: Non-static methods operate on instance variables and can access other non-static members of the class.
2. **Object Dependency**: They can only be invoked through an object of the class.
3. **Can Access Both Static and Non-Static Members**: Unlike static methods, which can only directly access static members, non-static methods can access both.
4. **Memory Allocation**: Non-static methods are stored in the heap memory along with the object of the class.
5. **Supports Method Overriding**: Non-static methods can be overridden in subclasses.

## Syntax of a Non-Static Method
```java
class Example {
    int number = 10; // Instance variable
    
    // Non-static method
    void display() {
        System.out.println("Number: " + number);
    }
}

public class Main {
    public static void main(String[] args) {
        Example obj = new Example(); // Creating an instance
        obj.display(); // Calling the non-static method
    }
}
```
### Explanation
- `display()` is a **non-static method** inside the `Example` class.
- It accesses the instance variable `number`.
- The method is called using an object (`obj.display();`).

## Types of Non-Static Methods
### 1. **Instance Methods with Parameters and Return Type**
A non-static method can have parameters and return a value.
```java
class Calculator {
    int add(int a, int b) {
        return a + b;
    }
}

public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        int sum = calc.add(5, 10);
        System.out.println("Sum: " + sum);
    }
}
```

### 2. **Instance Methods Without Parameters and Return Type**
```java
class Greeting {
    void sayHello() {
        System.out.println("Hello, Welcome to Java!");
    }
}

public class Main {
    public static void main(String[] args) {
        Greeting greet = new Greeting();
        greet.sayHello();
    }
}
```

## Accessing Non-Static Methods in the Same Class
A non-static method in the same class can be accessed using `this` keyword or directly.
```java
class Demo {
    void show() {
        System.out.println("Inside show method");
    }
    void display() {
        show(); // Direct call
        this.show(); // Using 'this' keyword
    }
}
```

## Difference Between Static and Non-Static Methods
| Feature | Static Method | Non-Static Method |
|---------|--------------|------------------|
| Belongs to | Class | Object (Instance) |
| Access | Only static members | Both static and non-static members |
| Invocation | ClassName.method() | ObjectName.method() |
| Memory Allocation | Class area | Heap (with the object) |
| Method Overriding | Cannot be overridden | Can be overridden |

## Use Cases of Non-Static Methods
- **Encapsulation**: Non-static methods allow data hiding and controlled access.
- **Instance-Specific Operations**: Useful when behavior varies per object.
- **OOP Concepts**: Used in inheritance, method overriding, and polymorphism.

## Conclusion
Non-static methods play a crucial role in Java’s object-oriented paradigm. They allow interaction with instance variables and provide flexibility in programming. Understanding their behavior is essential for designing efficient Java applications.

