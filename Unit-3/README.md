<h1 align="center">Unit-3</h1>
<h1 align="center">Java New Features</h1>



### ➡️ Functional Interfaces
- A Functional Interface is an interface that contains only 1 abstract method.
- It can have any numnber of default, static method but only 1 number abstract method.
- Functional Interface are also called Single Abtract Method Interface or SAM Interface.

#### Example(s) -
```java
@FunctionalInterface
public interface MyInterface{

    // Abtract Method
    public void SayHello();
}
```
```java
@FunctionalInterface{
public static void main(String[] args){

    // Abtract Method
    public void SayHello();

    // Not an Abtract Method
    public void sayOk(){};
}
```


---


### ➡️ Lambda Expression
- In java, Lambda expression is an way to define anonymous function or method that can be passed around a value.
  ``` ( Anonymous Function - Function without any name. )```
- It allow you to write code in more concise and flexible way and easier to read.
- It is a shorthand notation of creating a instance of Functional Interface.

#### Syntax - 
```java
(paramter_N, .........., paratmeter_N) -> expresion

OR

(parameter) -> {body} 
```
- The body of the lambda expression can have 0 , 1 or more statements.
- The return type of the anonymous function is same as the value returned within the code block or void if nothing is returned.
- If one statement is there the curly brackets is not mandatory.

#### Example -
```java
// lambda Expression
(int a,int b) -> { System.out.println(a+b);
                   return a+b;}
```

#### Program (Code) -  
```java
import java.utit.*;
public class LamndaExpression{
    public static void main(String[] args){
    ArrayList<Integer> arr = new ArrayList<Integer>();
    arr.add(5);
    arr.add(4);
    arr.add(3);
    arr.add(2);
    arr.add(1);

    // Lambda Expression being used with forEach Method
    arr.forEach((n)-> System.out.println(n));
    }
}
```
#### Output
```
5
4
3
2
1
```


---


### ➡️ Method References

---


### ➡️ Stream API

---


### ➡️ Default Methods

---


### ➡️ Static Method

---


### ➡️ Base64 Encode and Decode

---


### ➡️ ForEach Method



### ➡️ Try-with resources
- `Try-with-resource` is a try statement that declares one or more resources.
- Resouces is an object that must be closed after finishing the program.
- The try-with-resouce statement ensure that each resouce is closed at the end of the statement execution. (means when the resoures must be closed when the code exection from the try block is finished)

#### Program
``` java
import java.io.*;
import java.util.*;

public class MyClass{
    public static void main(String[] args){
        try(FileOutputStream file = new FileOutputStream("abc.txt")){
            String message = "Welcome of Java";
            byte [] ByteArray = message.getBytes();
            file.write(ByteArray);
            System.out.println("Message written to file successfully.");  
        } catch(IOException e){
            System.out.println("Exception");
        }
    }
}
```
#### About -
- It uses an instance of FileOutputStream (here `file`) to write data into the file.
- FileOutputStream is a resource thet must be closed after the program is finished with it.
- So in this example, closing of resource is done by try itself.


---


### ➡️ Type Annotations

---


### ➡️ Repeating Annotations


---


### ➡️ Java Module System


---


### ➡️ Diamond Syntax with Inner Anonymous Class


---


### ➡️ Local Variable Type Inference
- Local variable type inference is a feature in Java that allows developers to declare local variables without specifying the type.
- The compiler will infer the type of the variable based on the initializer.
- This can make code more concise and easier to read.
- Here are the rules for local variable type inference:
  1. The variable must be declared with the var keyword.
  2. The variable must be initialized.
  3. The type of the initializer must be unambiguous.

#### Valid Code -
```java
var name = "John Doe";
```
- The compiler will infer that the type of the variable name is String. This is because the initializer is a string literal.

#### Invalid Code -
```java
var name;
```
- This is because the initializer is missing. The compiler cannot infer the type of the variable without an initializer.
> Local variable type inference is a powerful feature that can make Java code more concise and easier to read. However, it is important to use it correctly.


---


### ➡️ Switch Expressions


---


### ➡️ Yield Keyword

---


### ➡️ Text Blocks

- Introduced in Java 15, text blocks provide a cleaner and more readable way to define multi-line string literals compared to traditional string concatenation. Here's a breakdown of text blocks in Java:

#### Benefits:
1. **Reduced verbosity** : No more need for explicit new line characters (\n) or concatenation operators (+) for each line.
2. **Simplified escaping**: Text blocks handle most characters directly, eliminating the need for frequent escaping within the string.

#### Syntax:
A text block starts with three double quotation marks (""") followed by optional whitespaces and a newline character. The closing also uses three double quotes (""").

Here's an example comparing traditional string concatenation with a text block:

```java
// Traditional String Concatenation
String message = "This is a \n" +
               "multiline string \n" +
               "created with concatenation.";

// Text Block
String message = """
This is a 
multiline string 
created with a text block.
""";
```

#### Indentation handling:
Text blocks preserve indentation within the block. However, the leading indentation on all lines is considered part of the block's formatting and is stripped by the compiler. This ensures proper alignment within your code.

#### Escaping within text blocks:
- While text blocks handle most characters directly, you can still use escaping for special cases like including literal quotation marks within the string. Use a backslash (\) before the character to be interpreted literally.
- Additionally, text blocks support a new escape sequence \s to include whitespace characters that might otherwise be stripped during indentation handling.


---


### ➡️ Records


---


### ➡️ Sealed Classes 
- A sealed class in Java is a class that can only be extended by a limited set of classes. This is in contrast to a non-sealed class, which can be extended by any class.
- Sealed classes were introduced in Java 15, and they provide a number of benefits, including:
#### 1. Improved predictability:
Sealed classes make it clear which classes are allowed to extend them, which can help to prevent errors and improve code readability.
#### 2. Increased security:
Sealed classes can be used to restrict access to sensitive classes, which can help to improve the security of an application.
#### 3. Enhanced performance:
Sealed classes can be used to optimize the performance of an application by reducing the number of classes that need to be loaded and processed.

- To create a sealed class, you use the `sealed` keyword. You can then specify a list of permitted subclasses using the permits keyword.   
- **For example**, the following code shows a sealed class called Shape that can only be extended by the Circle, Square, and Triangle classes:
```java
public sealed class Shape permits Circle, Square, Triangle {
  // Class definition
}
```
> Any attempt to extend the `Shape` **class** from a class that is not listed in the `permits` clause will result in a **compile-time error**.

Sealed classes can also be used to seal interfaces. This means that only the classes listed in the permits clause can implement the interface. For example, the following code shows a sealed interface called Drawable that can only be implemented by the Circle, Square, and Triangle classes:

```java
public sealed interface Drawable permits Circle, Square, Triangle {
  // Interface definition
}
```

#### Program - 
```java
// Sealed Class
sealed class Abhinav permits Abhilesh, Patel{
    public void sayHello(){
        System.out.println("Hello");
    }
}


// Non Sealed Class
non-sealed class Abhilesh extends Abhinav{
    @Override
    public void sayHello(){
        System.out.println("Bye");
    }
}


// Non Sealed Class
non-sealed class Patel extends Abhinav{
    @Override
    public void sayHello(){
        System.out.println("Bye");
    }
}


public class SealedClasses {
    public static void main(String[] args) {

        // Creating Instance of sealed class
        Abhinav abhinav = new Abhinav();
        abhinav.sayHello();

        // Overriding sealed class with permits
        Abhilesh abhilesh = new Abhilesh();
        abhilesh.sayHello();

        Patel patel = new Patel();
        patel.sayHello();
    }
}

```
