# **Operators in Java**

### **What are Operators and Operands?**
In Java, **operators** are special symbols used to perform operations on variables and values. The **operand** is the value or variable on which the operator performs the operation.

### **Example**
```java
int a = 10 + 5;
```
Here:
- `+` is the **operator** (Addition Operator).
- `10` and `5` are **operands**.
- The result `15` is stored in `a`.

---

## **Types of Operators in Java**
Java provides several types of operators:

1. **Arithmetic Operators**
2. **Relational (Comparison) Operators**
3. **Logical Operators**
4. **Bitwise Operators**
5. **Assignment Operators**
6. **Increment & Decrement Operators**
7. **Ternary Operator**
8. **Instanceof Operator**
9. **Type Casting Operators**

Each of these operator types is explained below in detail.

## **1. Arithmetic Operators**
These operators are used to perform basic mathematical operations.

| Operator | Description | Example |
|----------|------------|---------|
| `+` | Addition | `a + b` |
| `-` | Subtraction | `a - b` |
| `*` | Multiplication | `a * b` |
| `/` | Division | `a / b` (Integer division truncates decimal part) |
| `%` | Modulus (Remainder) | `a % b` |

### **Example**
```java
public class ArithmeticExample {
    public static void main(String[] args) {
        int a = 10, b = 5;
        System.out.println("Addition: " + (a + b)); // 15
        System.out.println("Subtraction: " + (a - b)); // 5
        System.out.println("Multiplication: " + (a * b)); // 50
        System.out.println("Division: " + (a / b)); // 2
        System.out.println("Modulus: " + (a % b)); // 0
    }
}
```
---

## **2. Relational (Comparison) Operators**
These operators compare two values and return a boolean result (`true` or `false`).

| Operator | Description | Example |
|----------|------------|---------|
| `==` | Equal to | `a == b` |
| `!=` | Not equal to | `a != b` |
| `>` | Greater than | `a > b` |
| `<` | Less than | `a < b` |
| `>=` | Greater than or equal to | `a >= b` |
| `<=` | Less than or equal to | `a <= b` |

### **Example**
```java
public class RelationalExample {
    public static void main(String[] args) {
        int a = 10, b = 5;
        System.out.println(a == b); // false
        System.out.println(a != b); // true
        System.out.println(a > b);  // true
        System.out.println(a < b);  // false
        System.out.println(a >= b); // true
        System.out.println(a <= b); // false
    }
}
```
---

## **3. Logical Operators**
Used to perform logical operations, mainly used in decision-making.

| Operator | Description | Example |
|----------|------------|---------|
| `&&` | Logical AND | `(a > 5 && b < 10)` |
| `\|\|` | Logical OR | `(a > 5 \|\| b < 2)` |
| `!` | Logical NOT | `!(a > 5)` |

### **Example**
```java
public class LogicalExample {
    public static void main(String[] args) {
        int a = 10, b = 5;
        System.out.println((a > 5 && b < 10)); // true
        System.out.println((a > 5 || b < 2));  // true
        System.out.println(!(a > 5));          // false
    }
}
```
---

## **4. Bitwise Operators**
Used to perform bit-level operations.

| Operator | Description | Example |
|----------|------------|---------|
| `&` | Bitwise AND | `a & b` |
| `\|`| Bitwise OR | `a \| b` |
| `^` | Bitwise XOR | `a ^ b` |
| `~` | Bitwise Complement | `~a` |
| `<<` | Left Shift | `a << 2` |
| `>>` | Right Shift | `a >> 2` |

### **Example**
```java
public class BitwiseExample {
    public static void main(String[] args) {
        int a = 5, b = 3; // 5 -> 0101, 3 -> 0011
        System.out.println("Bitwise AND: " + (a & b)); // 0001 -> 1
        System.out.println("Bitwise OR: " + (a | b));  // 0111 -> 7
        System.out.println("Bitwise XOR: " + (a ^ b)); // 0110 -> 6
        System.out.println("Bitwise Complement: " + (~a)); // -6
        System.out.println("Left Shift: " + (a << 1)); // 1010 -> 10
        System.out.println("Right Shift: " + (a >> 1)); // 0010 -> 2
    }
}
```
---

## **5. Assignment Operators**
Used to assign values to variables.

| Operator | Description | Example |
|----------|------------|---------|
| `=` | Assign | `a = 10` |
| `+=` | Add and assign | `a += 5` (same as `a = a + 5`) |
| `-=` | Subtract and assign | `a -= 5` (same as `a = a - 5`) |
| `*=` | Multiply and assign | `a *= 5` (same as `a = a * 5`) |
| `/=` | Divide and assign | `a /= 5` (same as `a = a / 5`) |
| `%=` | Modulus and assign | `a %= 5` (same as `a = a % 5`) |

### **Example**
```java
public class AssignmentExample {
    public static void main(String[] args) {
        int a = 10;
        a += 5; // a = 15
        System.out.println(a);
        a *= 2; // a = 30
        System.out.println(a);
        a -= 5; // a = 25
        System.out.println(a);
    }
}
```
---

## **6. Increment & Decrement Operators**
Used to increase or decrease the value of a variable.

| Operator | Description | Example |
|----------|------------|---------|
| `++` | Increment | `a++` (Post-increment) / `++a` (Pre-increment) |
| `--` | Decrement | `a--` (Post-decrement) / `--a` (Pre-decrement) |

### **Example**
```java
public class IncrementExample {
    public static void main(String[] args) {
        int a = 5;
        System.out.println(a++); // 5 (then a becomes 6)
        System.out.println(++a); // 7
        System.out.println(a--); // 7 (then a becomes 6)
        System.out.println(--a); // 5
    }
}
```
---

## **7. Ternary Operator**
Used as a shorthand for if-else statements.

| Operator | Description | Example |
|----------|------------|---------|
| `? :` | Ternary | `result = (a > b) ? a : b;` |

### **Example**
```java
public class TernaryExample {
    public static void main(String[] args) {
        int a = 10, b = 20;
        int max = (a > b) ? a : b;
        System.out.println("Maximum: " + max);
    }
}
```
---

## **8. Instanceof Operator**
Used to check if an object belongs to a specific class.

### **Example**
```java
class Animal { }
class Dog extends Animal { }

public class InstanceofExample {
    public static void main(String[] args) {
        Dog d = new Dog();
        System.out.println(d instanceof Dog); // true
        System.out.println(d instanceof Animal); // true
    }
}
```
---

## **9. Type Casting Operators**
Used to convert one data type into another.

### **Example**
```java
public class TypeCastingExample {
    public static void main(String[] args) {
        int a = 10;
        double b = a; // Implicit Casting
        System.out.println(b);
        
        double c = 9.78;
        int d = (int) c; // Explicit Casting
        System.out.println(d);
    }
}
```
