## Array List
- Dynamic Array

  ArrayList is a resizable array, which means it can grow and shrink in size automatically as you add or remove elements.

  
### ➡️ Key Characteristics
  
1. Flexible Size:

   Unlike regular arrays, ArrayList does not have a fixed size. It adjusts its capacity as needed when elements are added or removed.

3. Fast Access:

   Accessing elements by their index (e.g., list.get(index)) is very fast, with a time complexity of O(1).



```java
import java.util.ArrayList;

public class Main {
    public static void main(String[] args) {
        // Creating an ArrayList
        ArrayList<String> fruits = new ArrayList<>();

        // Adding elements
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Mango");

        // Accessing elements
        System.out.println(fruits.get(0)); // Output: Apple

        // Modifying elements
        fruits.set(1, "Grapes");

        // Removing elements
        fruits.remove(0); 

        // Iterating through the list
        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}

```

## Linked List

- Linked list is a linear data structure where data are not stored sequentially inside the computer memory but they are link with each other by the address.

  
- Doubly Linked List:

  LinkedList is a sequence of nodes where each node contains a reference to the previous and next node, allowing for efficient insertions and deletions.

- The best choice of linked list is deletion and insertion and worst choice is retrieval.
- In Linked list random access is not allowed . It traverse through iterator.




### ➡️ Key Characteristics
- **Dynamic Size**: Automatically adjusts its size by adding or removing nodes.
- **Fast Insertions/Deletions**: Adding or removing elements at the beginning or end, or from the middle of the list, is fast with a time complexity of O(1).
- **Slower Access**: Accessing elements by their index (e.g., list.get(index)) is slower, with a time complexity of O(n), because it may require traversing the list from the beginning or end.
  
### ➡️ Operations
- **Adding Elements**:
- 
  add(element), add(index, element), addFirst(element), and addLast(element).
- **Removing Elements**:
- 
   remove(index), remove(element), removeFirst(), and removeLast().
- **Modifying Elements**:
- 
  set(index, element).
- **Retrieving Elements**:
- 
   get(index), getFirst(), and getLast().


```java
import java.util.LinkedList;

public class Main {
    public static void main(String[] args) {
        // Creating a LinkedList
        LinkedList<String> fruits = new LinkedList<>();

        // Adding elements
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");
        fruits.addFirst("Mango"); // Adding at the beginning
        fruits.addLast("Peach");  // Adding at the end

        // Accessing elements
        System.out.println(fruits.get(0)); // Output: Mango

        // Modifying elements
        fruits.set(1, "Blueberry");

        // Removing elements
        fruits.remove(0);
        fruits.removeLast();

        // Iterating through the list
        for (String fruit : fruits) {
            System.out.println(fruit);
        }
    }
}
```
When to Use
Use LinkedList when you need a list that allows for fast insertions and deletions, especially at the beginning or end.
Ideal for scenarios where elements are frequently added or removed, and random access is less important.



## Vector
