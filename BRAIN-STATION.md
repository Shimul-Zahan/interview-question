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

# 4. Which two words are closest in meaning?
- **Options:**
  - a) qualified, practicable
  - b) practicable, feasible
  - c) practicable, puissant
  - d) feasible, mundane
- **Answer:** b) practicable, feasible
- **Explanation:** As explained above, both "practicable" and "feasible" refer to something that is possible or capable of being done.

---

# 5. Which of the following algorithms is used for searching in a sorted array?
- **Options:**
  - a) Exponential Search
  - b) Binary Search
  - c) Jump Search
  - d) Linear Search
- **Answer:** b) Binary Search
- **Explanation:** **Binary Search** is the most efficient algorithm for searching in a sorted array. It works by repeatedly dividing the search space in half, thus reducing the number of comparisons, with a time complexity of O(log n).

---

# 6. You need to find the shortest path between two nodes in an unweighted graph. Which algorithm would you use?
- **Options:**
  - a) Use Breadth-First Search (BFS)
  - b) Use Dijkstra's Algorithm
  - c) Use A* Search
  - d) Use Depth-First Search (DFS)
- **Answer:** a) Use Breadth-First Search (BFS)
- **Explanation:** **BFS** is ideal for finding the shortest path in an **unweighted graph** because it explores nodes level by level and guarantees the shortest path. Dijkstra's algorithm and A* are used for weighted graphs, and DFS is not efficient for finding the shortest path.

---

# 7. What is the way to access a method of a class without creating an object of the class?
- **Options:**
  - a) By instantiating the class
  - b) By calling the method directly
  - c) None of the above
  - d) Using static method
- **Answer:** d) Using static method
- **Explanation:** A **static method** can be called on a class without creating an instance of that class. Static methods are defined using the `@staticmethod` decorator in Python and can be accessed using the class name directly.

---

# 8. What code number could be assigned to CARDANO if ETHEREUM was given the number 95?
- **Options:**
  - a) 55
  - b) 65
  - c) 56
  - d) 66
- **Answer:** c) 56
- **Explanation:** This question likely refers to a cryptographic or custom mapping system, but based on the options, **56** seems to be the appropriate code number for CARDANO.

---

# 9. A pointer to the base class can hold the address of:
- **Options:**
  - a) Only derived class object
  - b) Base class object as well as derived class object
  - c) None of the above
  - d) Only base class object
- **Answer:** b) Base class object as well as derived class object
- **Explanation:** In **Object-Oriented Programming**, a base class pointer can hold the address of both a base class object and a derived class object due to **polymorphism**. This is a feature of inheritance in OOP.

---

# 10. I am an odd number. Take away a letter and I become even. What number am I?
- **Options:**
  - a) 9
  - b) 11
  - c) 7
  - d) 3
- **Answer:** b) 11
- **Explanation:** The number **11** is odd. If you remove the letter **S** from "Seven," you are left with the word "even," which is an even number.

---

# 11. A man walks 5 miles south, then 5 miles east, and finally, 5 miles north. In which direction is he from his starting point?
- **Options:**
  - a) South
  - b) West
  - c) East
  - d) North
- **Answer:** d) North
- **Explanation:** The man walks 5 miles south, 5 miles east, and then 5 miles north. If you follow this path, he will end up in the **same** position as where he started. But since the question asks for the direction, after walking north, he will be directly in the **same place**.

---
