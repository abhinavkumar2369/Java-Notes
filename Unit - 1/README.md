<h1 align="center">Unit-3</h1>
<h1 align="center">Java New Features</h1>



## Functional Interfaces 🚀
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



## Lambda Expression 🚀
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

## Method References 🚀
## Stream API 🚀
## Default Methods 🚀
## Static Method 🚀
## Base64 Encode and Decode 🚀
## ForEach Method 🚀



## Try-with resources 🚀
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



## Type Annotations 🚀
## Repeating Annotations 🚀
## Java Module System 🚀
## Diamond Syntax with Inner Anonymous Class 🚀
## Local Variable Type Inference 🚀
## Switch Expressions 🚀
## Yield Keyword 🚀
## Text Blocks 🚀
## Records 🚀
## Sealed Classes 
