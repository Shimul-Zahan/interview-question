### Multiple-Choice Questions (MCQs) with Answers, Explanations, and Code Examples

#### 1. Which of the following refers to internal software equality?

**Options:**

- a. Scalability
- b. Usability
- c. Reliability
- d. Reusability

**Answer:** d. Reusability

**Explanation:**
Reusability refers to the capability of using software components in different systems or parts of the same system to enhance efficiency and maintainability. Internal equality in this context means having modular and reusable components.

---

#### 2. Which of the following options is not true about the Binary Search Tree (BST)?

**Options:**

- a. The value of the left child should be less than the root node
- b. The value of the right child should be greater than the root node
- c. The left and right subtrees should also be a binary search tree
- d. None of the above

**Answer:** d. None of the above

**Explanation:**
All given options about BST properties are correct. For a tree to qualify as a BST:
- The left child must have values less than the root.
- The right child must have values greater than the root.
- Both subtrees must independently follow the BST properties.

**Code Example:**
```python
class Node:
    def __init__(self, value):
        self.value = value
        self.left = None
        self.right = None

def insert(root, key):
    if root is None:
        return Node(key)
    if key < root.value:
        root.left = insert(root.left, key)
    else:
        root.right = insert(root.right, key)
    return root

root = None
root = insert(root, 10)
root = insert(root, 5)
root = insert(root, 20)
```

---

#### 3. A documented life cycle model helps to identify _____ in the development process.

**Options:**

- a. Omission
- b. Redundancies
- c. Inconsistencies
- d. All of the above

**Answer:** d. All of the above

**Explanation:**
A documented life cycle model, such as Waterfall or Agile, helps:
- Detect omissions in requirements or implementation.
- Eliminate redundant processes or components.
- Resolve inconsistencies in design or documentation.

---

#### 4. The main objective of a feasibility study is:

**Options:**

- a. To assess if it is possible to meet the requirements specified subject to constraints of budget, human resource, and hardware
- b. To remove bottlenecks in implementing the desired system
- c. To assess whether it is possible to meet the requirements specifications
- d. To assist the management in implementing the desired system

**Answer:** a. To assess if it is possible to meet the requirements specified subject to constraints of budget, human resource, and hardware

**Explanation:**
A feasibility study evaluates technical, financial, and operational constraints to determine whether a project is achievable and worth pursuing.

---

#### 5. What would be the minimum time complexity if we were to insert an element at the front of a linked list? Assume the head is known.

**Options:**

- a. O(1)
- b. O(n)
- c. O(n²)
- d. O(nlogn)

**Answer:** a. O(1)

**Explanation:**
Inserting an element at the front of a linked list only involves updating the head pointer, which is a constant-time operation.

**Code Example:**
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

def insert_at_front(head, data):
    new_node = Node(data)
    new_node.next = head
    return new_node

head = None
head = insert_at_front(head, 10)
head = insert_at_front(head, 20)
```

---

#### 6. Which statement is used to get all data from the student table whose name includes 'p'?

**Options:**

- a. `SELECT * FROM student WHERE name LIKE '_p%';`
- b. `SELECT * FROM student WHERE name LIKE '%p%';`
- c. `SELECT * FROM student WHERE name LIKE '_p';`
- d. `SELECT * FROM student WHERE name LIKE 'p%';`

**Answer:** b. `SELECT * FROM student WHERE name LIKE '%p%';`

**Explanation:**
The `%` wildcard in SQL matches any sequence of characters, while `_` matches a single character. The query fetches rows where the name contains the letter 'p' anywhere.

**Code Example:**
```sql
SELECT * FROM student WHERE name LIKE '%p%';
```

---

#### 7. When searching for the key value 60 in a binary search tree, nodes containing the key values 10, 20, 40, 50, 70, 80, 90 are traversed. How many different orders are possible in which these key values can occur on the search path from the root to the node containing the value 60?

**Options:**

- a. 5040
- b. 35
- c. 64
- d. 128

**Answer:** b. 35

**Explanation:**
The number of different orders is based on the permutations of the elements traversed while maintaining the BST properties.

---

#### 8. Which feature of OOPS can be used to reduce code redundancy?

**Options:**

- a. Abstraction
- b. Inheritance
- c. Encapsulation
- d. Polymorphism

**Answer:** b. Inheritance

**Explanation:**
Inheritance allows a class to reuse methods and attributes of a parent class, reducing redundancy.

**Code Example:**
```python
class Parent:
    def common_function(self):
        return "This is reusable code"

class Child(Parent):
    pass

child_instance = Child()
print(child_instance.common_function())
```

---

#### 9. You need to sort a large dataset that fits entirely in memory, and you want the algorithm to be fast in the average case.

**Options:**

- a. Use Selection Sort
- b. Use Bubble Sort
- c. Use Merge Sort
- d. Use Quick Sort

**Answer:** d. Use Quick Sort

**Explanation:**
Quick Sort has an average-case time complexity of O(nlogn) and is faster for in-memory datasets compared to other options.

**Code Example:**
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

data = [3, 6, 8, 10, 1, 2, 1]
print(quick_sort(data))

---

# 1. Which of the following is the next letter in the series? A, D, G, J, M, ?
- **Options:**
  - a) P
  - b) N
  - c) O
  - d) Q
- **Answer:** a) P
- **Explanation:** The letters are increasing by 3 positions each time in the alphabet.
  - A (1st), D (4th), G (7th), J (10th), M (13th).
  The next letter is the 16th letter, which is **P** (13 + 3 = 16).

---

# 2. Which of the following statements is correct to display all the students with the name, address, and age whose age is in the range of 15 to 20 from the 'student' table?
- **Options:**
  - a) `SELECT * FROM student WHERE age IN (15 to 20)`
  - b) `SELECT * FROM student WHERE age NOT IN (15 AND 20)`
  - c) `SELECT * FROM student WHERE age BETWEEN 15 AND 20`
  - d) `SELECT * FROM student WHERE age NOT BETWEEN 15 AND 20`
- **Answer:** c) `SELECT * FROM student WHERE age BETWEEN 15 AND 20`
- **Explanation:** The `BETWEEN` keyword is used in SQL to filter records within a range. It is inclusive of the boundary values, so it will select students whose age is between 15 and 20, inclusive.

---

# 3. Which two words are closest in meaning?
- **Options:**
  - a) qualified, practicable
  - b) practicable, feasible
  - c) practicable, puissant
  - d) feasible, mundane
- **Answer:** b) practicable, feasible
- **Explanation:** Both "practicable" and "feasible" mean something that is achievable or possible to do. These words are used in contexts where something can be implemented or achieved.

---

# 4. Which of the following algorithms is used for searching in a sorted array?
- **Options:**
  - a) Exponential Search
  - b) Binary Search
  - c) Jump Search
  - d) Linear Search
- **Answer:** b) Binary Search
- **Explanation:** **Binary Search** is the most efficient algorithm for searching in a sorted array. It works by repeatedly dividing the search space in half, thus reducing the number of comparisons, with a time complexity of O(log n).

---

# 5. You need to find the shortest path between two nodes in an unweighted graph. Which algorithm would you use?
- **Options:**
  - a) Use Breadth-First Search (BFS)
  - b) Use Dijkstra's Algorithm
  - c) Use A* Search
  - d) Use Depth-First Search (DFS)
- **Answer:** a) Use Breadth-First Search (BFS)
- **Explanation:** **BFS** is ideal for finding the shortest path in an **unweighted graph** because it explores nodes level by level and guarantees the shortest path. Dijkstra's algorithm and A* are used for weighted graphs, and DFS is not efficient for finding the shortest path.

---

# 6. What is the way to access a method of a class without creating an object of the class?
- **Options:**
  - a) By instantiating the class
  - b) By calling the method directly
  - c) None of the above
  - d) Using static method
- **Answer:** d) Using static method
- **Explanation:** A **static method** can be called on a class without creating an instance of that class. Static methods are defined using the `@staticmethod` decorator in Python and can be accessed using the class name directly.

---

# 7. What code number could be assigned to CARDANO if ETHEREUM was given the number 95?
- **Options:**
  - a) 55
  - b) 65
  - c) 56
  - d) 66
- **Answer:** c) 56
- **Explanation:** This question likely refers to a cryptographic or custom mapping system, but based on the options, **56** seems to be the appropriate code number for CARDANO.

---

# 8. A pointer to the base class can hold the address of:
- **Options:**
  - a) Only derived class object
  - b) Base class object as well as derived class object
  - c) None of the above
  - d) Only base class object
- **Answer:** b) Base class object as well as derived class object
- **Explanation:** In **Object-Oriented Programming**, a base class pointer can hold the address of both a base class object and a derived class object due to **polymorphism**. This is a feature of inheritance in OOP.

---

# 9. I am an odd number. Take away a letter and I become even. What number am I?
- **Options:**
  - a) 9
  - b) 11
  - c) 7
  - d) 3
- **Answer:** b) 11
- **Explanation:** The number **11** is odd. If you remove the letter **S** from "Seven," you are left with the word "even," which is an even number.

---

# 10. A man walks 5 miles south, then 5 miles east, and finally, 5 miles north. In which direction is he from his starting point?
- **Options:**
  - a) South
  - b) West
  - c) East
  - d) North
- **Answer:** d) North
- **Explanation:** The man walks 5 miles south, 5 miles east, and then 5 miles north. If you follow this path, he will end up in the **same** position as where he started. But since the question asks for the direction, after walking north, he will be directly in the **same place**.

---

# 11. Which of the following is correct to display all students with name, address, and age whose age is in the range of 15 to 20?
- **Options:**
  - a) `SELECT * FROM student WHERE age IN (15 to 20)`
  - b) `SELECT * FROM student WHERE age NOT IN (15 AND 20)`
  - c) `SELECT * FROM student WHERE age BETWEEN 15 AND 20`
  - d) `SELECT * FROM student WHERE age NOT BETWEEN 15 AND 20`
- **Answer:** c) `SELECT * FROM student WHERE age BETWEEN 15 AND 20`
- **Explanation:** The `BETWEEN` keyword in SQL is used to filter records that fall within a specific range. Here, it retrieves students whose age is between 15 and 20, inclusive.




## 1. Which class instance cannot be created?

**Options:**

- a. Abstract class
- b. Base class
- c. Anonymous class
- d. Virtual class

**Answer:** a. Abstract class

**Explanation:**
An **abstract class** cannot be instantiated directly because it may contain one or more abstract methods, which are methods declared without implementation. These methods need to be implemented by a subclass. Abstract classes provide a blueprint for other classes, but you can only create instances of non-abstract subclasses that implement the abstract methods.

---

## 2. What is normalization in a database?

**Options:**

- a. The process of adding redundant data to a table
- b. The process of removing redundant data from a table
- c. The process of optimizing data in a table
- d. The process of organizing data in a table

**Answer:** b. The process of removing redundant data from a table

**Explanation:**
**Normalization** is a database design technique that aims to minimize redundancy and dependency by organizing fields and tables of a database. The process involves decomposing a table into smaller, related tables and ensuring that each piece of information is stored in one place, thus reducing the chances of having duplicate data.

---

## 3. A duck is behind another duck. Another duck is in front of a duck. A third duck is in the middle of two ducks. What is the minimum number of ducks required to meet these criteria?

**Answer:** 3

**Explanation:**
To meet all the given criteria:
- Duck 1 is behind Duck 2.
- Duck 2 is in front of Duck 1.
- Duck 3 is between Duck 1 and Duck 2.
Therefore, only 3 ducks are necessary to meet the condition: Duck 1, Duck 2, and Duck 3.

---

## 4. Which of the following statements is correct to display all the students with the name, address, and age whose age is in the range of 15 to 20 from the 'student' table?

**Options:**

- a. `SELECT * FROM student WHERE age NOT BETWEEN 15 AND 20`
- b. `SELECT * FROM student WHERE age NOT IN (15 AND 20)`
- c. `SELECT * FROM student WHERE age BETWEEN 15 AND 20`
- d. `SELECT * FROM student WHERE age IN (15 to 20)`

**Answer:** c. `SELECT * FROM student WHERE age BETWEEN 15 AND 20`

**Explanation:**
The `BETWEEN` keyword in SQL is used to select values within a given range. It is inclusive, meaning it includes both 15 and 20 in the range. Therefore, the correct SQL query to retrieve students whose age is between 15 and 20 is `SELECT * FROM student WHERE age BETWEEN 15 AND 20`.

---

## 5. Which of the following is/are correct in-order traversal sequence(s) of binary search tree(s)?

**Options:**

- a. 4, 6, 7, 12, 9, 18, 20
- b. 5, 8, 9, 12, 10, 15, 25
- c. 7, 10, 8, 14, 16, 20
- d. 3, 5, 7, 8, 15, 19, 25

**Answer:** b. 5, 8, 9, 12, 10, 15, 25

**Explanation:**
In-order traversal of a **binary search tree (BST)** visits nodes in ascending order. For a BST, this means visiting the left subtree, then the node, then the right subtree. For the given sequences, only option **b** represents a valid in-order traversal where the values are arranged in increasing order.

---

## 6. Explain the concept of an interface in OOP and its significance.

**Options:**

- a. An interface is a concrete class that provides a default implementation for methods.
- b. An interface is a collection of method signatures without any implementation.
- c. An interface is a way to encapsulate data within a class.
- d. An interface is a type of inheritance used to extend a class.

**Answer:** b. An interface is a collection of method signatures without any implementation.

**Explanation:**
An **interface** in Object-Oriented Programming (OOP) is a contract that defines a set of methods but does not provide their implementation. Classes that implement this interface must provide the actual implementations of these methods. Interfaces are used to achieve **abstraction** and **polymorphism**. They allow different classes to follow a common interface while implementing the behavior differently.

---

## 7. What is the main difference between a process and a thread?

**Options:**

- a. A process can run on multiple processors, while a thread can only run on one processor.
- b. A process can run independently, while a thread must be part of a process.
- c. A process has its own memory space, while a thread shares memory with other threads.
- d. A process can have multiple threads, while a thread can only belong to one process.

**Answer:** b. A process can run independently, while a thread must be part of a process.

**Explanation:**
A **process** is an independent unit of execution that has its own memory space. It runs on its own and can have multiple threads running within it. A **thread**, on the other hand, is a unit of execution within a process. All threads within the same process share the same memory space, which allows them to communicate with each other easily.

---

## 8. Which class cannot create its instance?

**Options:**

- a. Anonymous class
- b. Nested class
- c. Abstract class
- d. Parent class

**Answer:** c. Abstract class

**Explanation:**
An **abstract class** cannot be instantiated because it may contain abstract methods that have no implementation. The purpose of an abstract class is to provide a base for other classes to inherit from and implement those abstract methods. Instances can only be created from concrete (non-abstract) classes that provide implementations for all abstract methods.

---

## 9. What is the name of the approach that follows step-by-step instructions for solving a problem?

**Options:**

- a. Sequential Structure
- b. A List
- c. An Algorithm
- d. A Plan

**Answer:** c. An Algorithm

**Explanation:**
An **algorithm** is a finite set of well-defined, step-by-step instructions used to solve a problem or perform a task. It is the most precise way to define how to process data and produce a result.

---

## 10. Which of the following is the best way to achieve both abstraction and code reusability in OOP?

**Options:**

- a. Using global variables
- b. Using function overloading
- c. Using inheritance
- d. Using abstract classes

**Answer:** d. Using abstract classes

**Explanation:**
Abstract classes provide a way to achieve both **abstraction** and **code reusability**. An abstract class allows you to define a common base with abstract methods, which must be implemented by subclasses. This ensures that specific behavior is defined while enabling code reuse by inheriting from the abstract class.

---

## 11. Find five consecutive numbers below that total 22.

**Options:**

- a. 7, 39, 64, 1, 37
- b. 93, 54, 1, 7, 6
- c. 5, 4, 1, 7, 6
- d. 5, 4, 3, 6, 8

**Answer:** c. 5, 4, 1, 7, 6

**Explanation:**
Adding the numbers 5, 4, 1, 7, and 6 results in a sum of 22 (5 + 4 + 1 + 7 + 6 = 22). Thus, option **c** is the correct answer.

---

## 12. Which statement is true?

**Options:**

- a. WHERE and HAVING clause filter rows
- b. Both WHERE and HAVING can be used in the same query
- c. WHERE and HAVING clause can be used interchangeably in any case

**Answer:** b. Both WHERE and HAVING can be used in the same query

**Explanation:**
Both `WHERE` and `HAVING` can be used in the same SQL query, but they apply at different stages:
- **WHERE** filters rows before any aggregation takes place.
- **HAVING** filters rows after aggregation (usually in a `GROUP BY` query).

---

## 13. What is the purpose of the HAVING clause in SQL?

**Options:**

- a. To filter the results of a query based on aggregate calculations
- b. To perform aggregate calculations on data
- c. To update data in a table
- d. To retrieve data from multiple tables

**Answer:** a. To filter the results of a query based on aggregate calculations

**Explanation:**
The `HAVING` clause is used to filter the results after an aggregate function, such as `COUNT()`, `SUM()`, `AVG()`, etc., has been applied. It is often used in conjunction with the `GROUP BY` clause.

---

## 14. For an undirected graph G with N vertices and E edges, the sum of the degrees of each vertex is:

**Options:**

- a. 2E
- b. NE
- c. N²
- d. E

**Answer:** a. 2E

**Explanation:**
In an undirected graph, each edge contributes two to the sum of degrees (one for each endpoint). Therefore, the sum of the degrees of all vertices is always equal to **2E**, where **E** is the number of edges in the graph.



---

## 15. What is the output of the following bitwise operations?

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 1;
    cout << (x << 1) << endl;
    return 0;
}

---

```cpp
#include <iostream>
using namespace std;

int main() {
    int arr[] = {1, 2, 3, 4, 5};
    int *p = arr;
    int *q = arr + 2;
    cout << *(q + 1) << endl;
    return 0;
}
**Answer:** 4

**Explanation: In the given code:**

-arr is an array of integers with values {1, 2, 3, 4, 5}.
-p points to the first element of the array.
-q points to the third element (index 2) of the array.
-The expression *(q + 1) means dereferencing the pointer q + 1, which moves the pointer from -the third element (which is 3) to the fourth element (which is 4). Thus, the output is 4

---

```cpp
#include <iostream>
using namespace std;

int main() {
    int total = 16;
    int count = 0;
    while (total > 1) {
        total /= 2;
        count++;
    }
    return 0;
}

**Options:**

-a. O(N^2)
-b. O(N/2)
-c. O(log N)
-d. O(N)
**Answer:** c. O(log N)

**Explanation:**
 -In the given code, total is being halved in each iteration of the while loop (total /= 2). This means the loop will continue running for log(total) iterations, which is O(log N) in time complexity. As the value of total is halved until it becomes 1, the time complexity grows logarithmically with respect to the input size.