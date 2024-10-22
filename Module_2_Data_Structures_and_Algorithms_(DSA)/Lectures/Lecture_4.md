# Lecture: 4. Linked Lists: Singly and Doubly Linked

## 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand the structure and functionality of singly and doubly linked lists.
- Implement basic operations (insertion, deletion, traversal) for both types of linked lists in Python.
- Recognize the advantages and disadvantages of linked lists compared to other data structures.

## 2. Introduction:
Linked lists are a fundamental data structure in computer science, crucial for efficient data management and manipulation. In this lecture, we will explore singly and doubly linked lists, which are essential for mastering data structures and algorithms (DSA). Understanding these concepts will not only enhance your coding skills in Python but also strengthen your foundation in databases and AI technologies.

Imagine a soccer team like Chelsea F.C. Each player (node) has a unique position (data) and a connection to the next player (next node). Just as players need to work together to create effective plays, linked lists allow data elements to be connected dynamically, enabling efficient data operations. This analogy will help you appreciate how linked lists function in various applications, including those relevant to sports analytics and game development.

## 3. Core Concepts:

### 3.1 Singly Linked Lists:
- **Definition**: A singly linked list consists of nodes where each node contains data and a reference (link) to the next node in the sequence.
- **Structure**:
  - **Node**: Contains two parts: data and next (pointer to the next node).
  - **Head**: The first node in the list.
  - **Tail**: The last node, which points to null.
  
- **Operations**:
  - **Insertion**: Adding a new node at the beginning, end, or after a given node.
  - **Deletion**: Removing a node by adjusting pointers.
  - **Traversal**: Visiting each node from head to tail.

### 3.2 Doubly Linked Lists:
- **Definition**: A doubly linked list allows traversal in both directions, with each node containing references to both the next and previous nodes.
- **Structure**:
  - **Node**: Contains three parts: data, next (pointer to the next node), and prev (pointer to the previous node).
  
- **Operations**:
  - **Insertion**: Similar to singly linked lists but requires updating both next and prev pointers.
  - **Deletion**: More efficient than singly linked lists due to direct access to the previous node.
  - **Traversal**: Can be performed forwards or backwards.

## 4. Practical Application:
In the context of Premier League Soccer analytics, linked lists can be used to manage player statistics over a season. For example, you can create a singly linked list where each node represents a match with player performance data. This allows for efficient insertion of new matches and quick access to player stats.

### Code Snippet Example (Singly Linked List):
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class SinglyLinkedList:
    def __init__(self):
        self.head = None
    
    def insert(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def display(self):
        current = self.head
        while current:
            print(current.data)
            current = current.next

# Example usage
team_stats = SinglyLinkedList()
team_stats.insert("Match 1: Chelsea vs. Arsenal - Win")
team_stats.insert("Match 2: Chelsea vs. Liverpool - Draw")
team_stats.display()
```

## 5. Summary:
In this lecture, we learned about singly and doubly linked lists, their structures, and key operations. We explored their applications in managing dynamic data, such as player statistics in soccer. Remember that mastering these concepts is vital for your journey in DSA, especially as you aim to optimize your Python code.

## 6. Next Steps:
In our next lecture, we will delve into more advanced data structures such as trees and graphs, which build upon the concepts learned today. To prepare, review the operations covered in this lecture and consider how linked lists might be utilized in other applications you encounter in gaming or sports analytics.