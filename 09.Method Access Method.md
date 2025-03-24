

#  Method Access Method
In Java, methods can be **static** or **non-static (instance methods)**. How one method calls another depends on whether they are static or non-static.

There are four possible combinations when one method tries to access another:

---

## **1. Static Method Calling Another Static Method**
- Both are class-level methods stored in the **static memory area**.
- A static method can call another static method **directly** without creating an object.  
#### Example:
```java
class MyClass {
    static void methodA() {
        methodB();  // Direct call
    }

    static void methodB() {
        System.out.println("Static Method B");
    }

    public static void main(String[] args) {
        methodA();  // Calling static method from main
    }
}
```

---

## **2. Non-Static Method Calling a Static Method**
- A non-static (instance) method can call a static method **directly**.
- Since static methods belong to the class, they are accessible from any instance.  
#### Example:
```java
class MyClass {
    void methodA() {
        methodB();  // Direct call
    }

    static void methodB() {
        System.out.println("Static Method B");
    }

    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.methodA();  // Calling non-static method
    }
}
```

---

## **3. Static Method Calling a Non-Static Method**
- A static method **cannot** directly call a non-static method because non-static methods belong to an instance.
- To access a non-static method, an object must be created inside the static method.  
#### Example:
```java
class MyClass {
    static void methodA() {
        // methodB();  // Not allowed directly
        MyClass obj = new MyClass();
        obj.methodB();  // Correct way
    }

    void methodB() {
        System.out.println("Non-static Method B");
    }

    public static void main(String[] args) {
        methodA();  // Calling static method from main
    }
}
```

---

## **4. Non-Static Method Calling Another Non-Static Method**
- Non-static methods can call other non-static methods **directly** because they belong to the same object.  
#### Example:
```java
class MyClass {
    void methodA() {
        methodB();  // Direct call
    }

    void methodB() {
        System.out.println("Non-static Method B");
    }

    public static void main(String[] args) {
        MyClass obj = new MyClass();
        obj.methodA();  // Calling non-static method
    }
}
```

---

## **Summary**
| From → To            | Possible Without Object? | Explanation                                |
|----------------------|--------------------------|--------------------------------------------|
| Static → Static      | Yes                      | Both are class-level (static area)         |
| Non-Static → Static  | Yes                      | Non-static can access static easily        |
| Static → Non-Static  | No                       | Needs an object because non-static methods belong to instances |
| Non-Static → Non-Static | Yes                   | Both belong to the same object             |

