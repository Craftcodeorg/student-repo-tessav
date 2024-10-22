# Module Title: Data Structures and Algorithms (DSA)

## Example 1: Implementing a Stack Using Lists

### 1. Introduction
In this section, we will explore the concept of a stack, a fundamental data structure that follows the Last In First Out (LIFO) principle. Stacks are widely used in programming for various applications, including managing function calls, undo mechanisms in applications, and parsing expressions. 

In the context of your work in Robotics, semiconductors, and consumer electronics, stacks can help manage tasks such as command execution order, handling interrupts, or maintaining the state of devices. Understanding how to implement a stack using lists in Python will enhance your ability to solve complex problems efficiently.

### 2. Code Snippet
Below is a well-commented Python code snippet that demonstrates how to implement a stack using lists. This code includes error handling and follows best practices for clarity and maintainability.

```python
class Stack:
    def __init__(self):
        """Initialize an empty stack."""
        self.items = []

    def is_empty(self):
        """Check if the stack is empty."""
        return len(self.items) == 0

    def push(self, item):
        """Add an item to the top of the stack."""
        self.items.append(item)
        print(f"Pushed {item} onto the stack.")

    def pop(self):
        """Remove and return the top item of the stack. Raise an error if the stack is empty."""
        if self.is_empty():
            raise IndexError("Pop from an empty stack.")
        item = self.items.pop()
        print(f"Popped {item} from the stack.")
        return item

    def peek(self):
        """Return the top item of the stack without removing it. Raise an error if the stack is empty."""
        if self.is_empty():
            raise IndexError("Peek from an empty stack.")
        return self.items[-1]

    def size(self):
        """Return the number of items in the stack."""
        return len(self.items)

    def display(self):
        """Display the current items in the stack."""
        print("Current Stack:", self.items)

# Example usage
if __name__ == "__main__":
    my_stack = Stack()
    my_stack.push(1)
    my_stack.push(2)
    my_stack.push(3)
    my_stack.display()
    
    print("Top item:", my_stack.peek())
    my_stack.pop()
    my_stack.display()
```

### 3. Explanation
- **Class Definition**: The `Stack` class encapsulates all functionalities related to the stack.
- **Initialization**: The `__init__` method initializes an empty list to store stack items.
- **is_empty()**: This method checks if the stack is empty, returning a boolean value.
- **push(item)**: Adds an item to the top of the stack. It appends the item to the list and provides feedback.
- **pop()**: Removes and returns the top item. It raises an `IndexError` if attempting to pop from an empty stack, ensuring safe operations.
- **peek()**: Returns the top item without removing it, also raising an error if the stack is empty.
- **size()**: Returns the current number of items in the stack.
- **display()**: Prints the current items in the stack for easy visualization.

This implementation provides a clear understanding of how stacks operate, allowing you to manage data effectively in various applications within your field.

### 4. Application
In Robotics, stacks can be employed to manage command sequences for robotic arms or drones. For instance, when a robot receives multiple commands, it can push each command onto a stack. The robot will execute commands in reverse order (last command first), which is essential for tasks that require precise execution sequences, such as picking up an object and placing it at a different location.

In semiconductor manufacturing, stacks can be used to manage tasks such as processing orders or handling interrupts during production runs. By using stacks, engineers can ensure that critical tasks are completed in the correct order without losing track of pending operations.

In consumer electronics, stacks can help manage user interactions with devices, such as navigating through menus or handling undo actions in applications. This improves user experience by providing intuitive control over device functionalities.

### Integration
This content is structured with clear headings and sections to facilitate easy navigation and comprehension. The use of markdown formatting enhances readability and organization within your learning platform. 

By engaging with this example and understanding its significance, you will strengthen your foundation in data structures while applying these concepts to real-world scenarios relevant to your career goals in technology.