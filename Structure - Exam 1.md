# Different types of data structures  

![alt](https://techvidvan.com/tutorials/wp-content/uploads/sites/2/2020/03/collection-framework-hierarchy-in-java.jpg)

## Map
In Java, a `Map` is an interface from the Java Collections Framework that represents a collection of key-value pairs. It allows you to store and manage data in a way where each piece of data is associated with a unique key, which can be used to retrieve the corresponding value. Maps are widely used to store data in a structured manner and provide efficient data retrieval.

![alt](https://www.scaler.com/topics/images/iterate-hashmap-in-java_thumbnail.webp)

1. **HashMap**: This is one of the most commonly used implementations of the `Map` interface. It uses a hash table data structure to store key-value pairs. It provides fast access to values based on their keys, making it suitable for most use cases. However, it does not guarantee any specific order of key-value pairs.

	```java
	Map<String, Integer> hashMap = new HashMap<>();
	hashMap.put("Alice", 25);
	hashMap.put("Bob", 30);
	hashMap.put("Charlie", 28);
    ```

2. **TreeMap**: This implementation uses a Red-Black tree data structure to store key-value pairs in sorted order based on the keys. As a result, the key-value pairs are stored in ascending order.

	```java
	Map<String, Integer> treeMap = new TreeMap<>();
	treeMap.put("Alice", 25);
	treeMap.put("Bob", 30);
	treeMap.put("Charlie", 28);
    ```

**Some common operations you can perform with a `Map` include:**

-   `put(key, value)`: Associates the specified value with the specified key in the map.
-   `get(key)`: Retrieves the value associated with the specified key.
-   `containsKey(key)`: Checks if the map contains a specific key.
-   `remove(key)`: Removes the key-value pair associated with the specified key.
-   `size()`: Returns the number of key-value pairs in the map.
-   `isEmpty()`: Checks if the map is empty.


```java
import java.util.HashMap;
import java.util.Map;

public class HashMapExample {
    public static void main(String[] args) {
        // Create a HashMap with key-value pairs of String (name) and Integer (age)
        Map<String, Integer> ageMap = new HashMap<>();

        // Add key-value pairs to the map
        ageMap.put("Alice", 25);
        ageMap.put("Bob", 30);
        ageMap.put("Charlie", 28);

        // Retrieve and print values based on keys
        String nameToFind = "Bob";
        int age = ageMap.get(nameToFind);
        System.out.println(nameToFind + "'s age is " + age);

        // Check if a key exists in the map
        String nameToCheck = "David";
        if (ageMap.containsKey(nameToCheck)) {
            System.out.println(nameToCheck + "'s age is " + ageMap.get(nameToCheck));
        } else {
            System.out.println(nameToCheck + " is not in the map.");
        }

        // Iterating through the map's key-value pairs
        System.out.println("Iterating through the map:");
        for (Map.Entry<String, Integer> entry : ageMap.entrySet()) {
            String name = entry.getKey();
            int personAge = entry.getValue();
            System.out.println(name + " is " + personAge + " years old.");
        }

        // Remove a key-value pair from the map
        String keyToRemove = "Bob";
        ageMap.remove(keyToRemove);
        System.out.println("After removing " + keyToRemove + ": " + ageMap);

        // Check if the map is empty
        System.out.println("Is the map empty? " + ageMap.isEmpty());
    }
}
```

## Set
In Java, a `Set` is a part of the Java Collections Framework and is an interface that represents a collection of unique elements. Unlike lists, which allow duplicate elements, **a `Set` does not allow duplicate elements**; it ensures that all elements within it are unique.

1. **HashSet**: This is one of the most commonly used implementations of the `Set` interface. It uses a hash table data structure to store elements, making it very efficient for adding, removing, and checking for the existence of elements. However, it does not guarantee any specific order of elements. 

	```java
	Set<String> hashSet = new HashSet<>();
	hashSet.add("apple");
	hashSet.add("banana");
	hashSet.add("cherry");
	```

2. **LinkedHashSet**: Similar to `HashSet`, but it maintains the order of elements as they were inserted. Elements are iterated in the order in which they were added.

	```java
	Set<String> linkedHashSet = new LinkedHashSet<>();
	linkedHashSet.add("apple");
	linkedHashSet.add("banana");
	linkedHashSet.add("cherry");
    ```

3. **TreeSet**: It guarantees that elements are stored in sorted (ascending) order. You can also provide a custom comparator to define the sorting criteria.

	```java
	Set<String> treeSet = new TreeSet<>();
	treeSet.add("banana");
	treeSet.add("cherry");
	treeSet.add("apple");
    ```

**Here are some common operations you can perform with sets:**

-   `add(element)`: Adds an element to the set if it's not already present.
-   `remove(element)`: Removes an element from the set.
-   `contains(element)`: Checks if an element is present in the set.
-   `size()`: Returns the number of elements in the set.
-   `isEmpty()`: Checks if the set is empty.

**Code Example**

```java
import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        // Create a HashSet of strings
        Set<String> fruitSet = new HashSet<>();

        // Adding elements to the set
        fruitSet.add("apple");
        fruitSet.add("banana");
        fruitSet.add("cherry");
        fruitSet.add("apple"); // Adding a duplicate element (ignored)

        System.out.println("Set elements: " + fruitSet);
        System.out.println("Set size: " + fruitSet.size());

        // Removing an element
        fruitSet.remove("banana");

        System.out.println("After removing 'banana': " + fruitSet);
        System.out.println("Set contains 'cherry': " + fruitSet.contains("cherry"));
        System.out.println("Set contains 'grape': " + fruitSet.contains("grape"));

        // Iterating through the set
        System.out.println("Iterating through the set:");
        for (String fruit : fruitSet) {
            System.out.println(fruit);
        }

        // Clearing the set
        fruitSet.clear();
        System.out.println("After clearing the set: " + fruitSet);
        System.out.println("Is the set empty? " + fruitSet.isEmpty());
    }
}
```

## Queue  
In Java, a queue is a linear data structure that follows the **First-In-First-Out (FIFO)** principle. This means that the first element added to the queue will be the first one to be removed. It can be thought of as a collection of elements with two primary operations:  
  
1.  **Enqueue**: This operation adds an element to the back (or rear) of the queue.  
2.  **Dequeue**: This operation removes and returns the element from the front of the queue.  
  
Additionally, there are two other common operations associated with a queue:  
  
3.  **Peek (or Front)**: This operation retrieves the element at the front of the queue without removing it.  
4.  **isEmpty**: This operation checks if the queue is empty.  
  
![alt](https://media.geeksforgeeks.org/wp-content/uploads/20220817115055/Queue-660x234.png)
  
**Code Example**  
  
```java  
import java.util.PriorityQueue;

public class PriorityQueueExample {
    public static void main(String[] args) {
        // Create a PriorityQueue of integers
        PriorityQueue<Integer> priorityQueue = new PriorityQueue<>();

        // Add elements to the PriorityQueue
        priorityQueue.offer(10);
        priorityQueue.offer(5);
        priorityQueue.offer(20);
        priorityQueue.offer(15);
        priorityQueue.offer(30);

        System.out.println("PriorityQueue elements: " + priorityQueue);

        // Poll and remove elements from the PriorityQueue in ascending order
        while (!priorityQueue.isEmpty()) {
            Integer element = priorityQueue.poll();
            System.out.println("Removed element: " + element);
        }
    }
}
```

### ArrayList
This is a widely used implementation of the `List` interface. It internally uses an array to store elements, offering efficient random access by index. `ArrayList` is suitable for scenarios where you frequently need to access elements by their position. However, it may be less efficient for insertions or deletions in the middle of the list.

### LinkedList
This is another implementation of the `List` interface. It uses a doubly-linked list internally to store elements. While `LinkedList` may be slower for random access by index, it excels at insertions and deletions, particularly in the middle of the list. It's a good choice when you need to manipulate the list frequently.

### Stack  
In Java, a stack is a linear data structure that follows the **Last-In-First-Out (LIFO)** principle. This means that the last element added to the stack is the first one to be removed. It can be thought of as a collection of elements with two primary operations:  
  
1.  **Push**: This operation adds an element to the top of the stack.  
2.  **Pop**: This operation removes and returns the top element from the stack.  
  
Additionally, there are two other common operations associated with a stack:  
  
4.  **Peek (or Top)**: This operation retrieves the top element from the stack without removing it.  
5.  **isEmpty**: This operation checks if the stack is empty.  
  
![alt](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20230726165552/Stack-Data-Structure.png)
  
**Code Example**  
  
```java  
import java.util.Stack;  
  
public class StackExample {  
    public static void main(String[] args) {  
        Stack<Integer> stack = new Stack<>();  
  
        // Push elements onto the stack  
        stack.push(1);  
        stack.push(2);  
        stack.push(3);  
  
        // Peek at the top element  
        int topElement = stack.peek();  
        System.out.println("Top element: " + topElement);  
  
        // Pop elements from the stack  
        int poppedElement = stack.pop();  
        System.out.println("Popped element: " + poppedElement);  
  
        // Check if the stack is empty  
        boolean isEmpty = stack.isEmpty();  
        System.out.println("Is the stack empty? " + isEmpty);  
  
        // Get the size of the stack  
        int stackSize = stack.size();  
        System.out.println("Stack size: " + stackSize);  
    }  
}  
```  

# Properties File

In Java, a properties file is a simple text file used to store configuration settings or key-value pairs in a human-readable format. Properties files are commonly used to configure Java applications, providing a way to externalize configuration and settings, making it easier to manage and modify application behavior without changing the source code.

```properties
# Database configuration
db.host=localhost
db.port=3306
db.username=myuser
db.password=mypassword
```

**Main methods used for properties files:**

1. `load(InputStream inputStream)`: Loads properties from an input stream (typically a file input stream) into the `Properties` object. This method reads the properties file in a specific format (usually key-value pairs) and populates the `Properties` object.

2. `getProperty(String key)`: Retrieves the value associated with a given key. If the key does not exist in the properties file, this method returns `null`.

**Code example**

```java
import java.io.FileInputStream;
import java.io.IOException;
import java.util.Properties;

public class PropertiesFileExample {
    public static void main(String[] args) throws IOException {
        Properties properties = new Properties();

        // Load the properties file
        properties.load(new FileInputStream("config.properties"));

        // Retrieve values from the properties file
        String dbHost = properties.getProperty("db.host");
        String dbPort = properties.getProperty("db.port");
        String dbUsername = properties.getProperty("db.username");
        String dbPassword = properties.getProperty("db.password");

        // Use the retrieved values
        System.out.println("Database Host: " + dbHost);
        System.out.println("Database Port: " + dbPort);
        System.out.println("Database Username: " + dbUsername);
        System.out.println("Database Password: " + dbPassword);

        // You can now use these properties in your application as needed.
        // For example, you can establish a database connection using these values.
    }
}
```

# Sort a list

In Java, you can sort a list of objects in several ways, depending on your requirements and the type of objects in the list. Here, I'll provide an example of how to sort a list of strings and a list of custom objects using different approaches.

## Sorting a List of Custom Objects from the entity class
To sort a list of custom objects, you can implement the `Comparable` interface in your custom class and override the `compareTo` method. This allows you to define the natural ordering of objects based on a specific criteria.

Here's an example with a custom `Person` class:

```java
import java.util.ArrayList;
import java.util.Collections;
import java.util.List;

class Person implements Comparable<Person> {
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public int compareTo(Person other) {
        // Compare based on age
        return Integer.compare(this.age, other.age);
    }

    @Override
    public String toString() {
        return name + " (" + age + " years old)";
    }
}

public class SortListOfCustomObjects {
    public static void main(String[] args) {
        List<Person> personList = new ArrayList<>();
        personList.add(new Person("Alice", 25));
        personList.add(new Person("Bob", 30));
        personList.add(new Person("Charlie", 28));

        // Sort the list based on age (natural ordering)
        Collections.sort(personList);

        // Print the sorted list
        for (Person person : personList) {
            System.out.println(person);
        }
    }
}
```

## Sorting a List of custom Objects using comparator
To sort a list of custom objects, you can use new comparator. This allows you to define the ordering of objects based on a specific criteria.

```java
playlist.getPlaylist().sort(new Comparator<Song>() {  
    @Override  
    public int compare(Song o1, Song o2) {  
        return o1.getName().compareTo(o2.getName());  
    }  
});
```

