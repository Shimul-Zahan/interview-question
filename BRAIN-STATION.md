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
