# if and if-else

Conditional statements in Java allow us to control the flow of execution based on conditions. 

---

## **1. `if` Statement**
- **`if` Statement** – Executes a block of code when a condition is `true`.

The `if` statement is the simplest conditional statement in Java. It checks whether a condition evaluates to `true` and executes the code inside its block. If the condition is `false`, the block is skipped.

### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
}
```
- The **condition** inside parentheses `( )` must be a boolean expression that evaluates to `true` or `false`.
- If the condition is `true`, the statements inside the curly braces `{ }` execute.
- If the condition is `false`, the block is skipped, and execution continues after the `if` statement.

### Flow - chart : 
![if](https://d1whtlypfis84e.cloudfront.net/guides/wp-content/uploads/2021/06/29085822/if-flowchart-606x1024.jpg "if")

### **Example 1: Checking if a number is positive**
```java
public class IfExample {
    public static void main(String[] args) {
        int number = 10;

        if (number > 0) { // Checks if the number is greater than 0
            System.out.println("The number is positive.");
        }

        System.out.println("End of program.");
    }
}
```

### **Output:**
```
The number is positive.
End of program.
```

**Explanation:**
- Since `number > 0` is `true`, the `if` block executes.
- The message **"The number is positive."** is printed.
- After the `if` block, execution continues normally.

---

### **Example 2: `if` Statement Skipping Execution**
```java
public class IfExample {
    public static void main(String[] args) {
        int number = -5;

        if (number > 0) { // This condition is false
            System.out.println("The number is positive.");
        }

        System.out.println("End of program.");
    }
}
```

### **Output:**
```
End of program.
```

**Explanation:**
- Since `number > 0` is `false`, the `if` block is skipped.
- The program simply prints **"End of program."**

---

## **2. `if-else` Statement**
-  **`if-else` Statement** – Executes one block if the condition is `true`, otherwise executes another block.

The `if-else` statement is used when we want to execute one block of code if the condition is `true` and another block if the condition is `false`.

### **Syntax:**
```java
if (condition) {
    // Code to execute if condition is true
} else {
    // Code to execute if condition is false
}
```
- If the condition is `true`, the code inside the `if` block executes.
- If the condition is `false`, the code inside the `else` block executes.

### Flow - chart : 
![if-else](https://d1whtlypfis84e.cloudfront.net/guides/wp-content/uploads/2021/06/29090322/if-else-flowchart.jpg "if-else")



### **Example 1: Checking if a number is positive or not**
```java
public class IfElseExample {
    public static void main(String[] args) {
        int number = -5;

        if (number > 0) { 
            System.out.println("The number is positive.");
        } else {
            System.out.println("The number is not positive.");
        }

        System.out.println("End of program.");
    }
}
```

### **Output:**
```
The number is not positive.
End of program.
```

**Explanation:**
- Since `number > 0` is `false`, the `else` block executes.
- The message **"The number is not positive."** is printed.

---

### **Example 2: Checking if a number is even or odd**
```java
public class EvenOddCheck {
    public static void main(String[] args) {
        int number = 7;

        if (number % 2 == 0) { // Checks if number is divisible by 2
            System.out.println("The number is even.");
        } else {
            System.out.println("The number is odd.");
        }

        System.out.println("End of program.");
    }
}
```

### **Output:**
```
The number is odd.
End of program.
```

**Explanation:**
- The condition `number % 2 == 0` checks if `7` is divisible by `2`.
- Since `7 % 2` equals `1`, the condition is `false`, so the `else` block executes.

---

### **Comparison: `if` vs. `if-else`**
| Feature | `if` Statement | `if-else` Statement |
|---------|---------------|---------------------|
| Executes a block if the condition is `true` | ✅ | ✅ |
| Skips execution if condition is `false` | ✅ | ❌ (Executes `else` block instead) |
| Handles alternative cases | ❌ | ✅ |
| Example Scenario | Check if a number is positive | Check if a number is positive or not |

---

## **Key Points to Remember**
1. The condition inside `if` or `if-else` must evaluate to `true` or `false`.
2. Curly braces `{ }` are **optional** for single-line statements but recommended for readability.
3. The `if` block executes only when the condition is `true`; otherwise, it is skipped.
4. The `if-else` ensures that one block always executes—either `if` or `else`.
