# Module Title: Data Structures and Algorithms (DSA)

## Example 2: Creating a Binary Search Tree

### 1. Introduction
In this section, we will explore the concept of a Binary Search Tree (BST), a crucial data structure that builds upon the foundational concepts of arrays and lists discussed in the previous lecture. Understanding BSTs is significant in fields such as Robotics, semiconductors, and consumer electronics, where efficient data retrieval and management are critical.

A Binary Search Tree is a hierarchical structure that allows for fast searching, inserting, and deleting of elements. In robotics, for instance, a BST can be used to efficiently manage sensor data or control commands. In semiconductors, it can help in organizing data related to component specifications. In consumer electronics, BSTs can be used in product catalogs or inventory management systems.

### 2. Code Snippet
Below is a well-commented Python code snippet illustrating the creation of a Binary Search Tree (BST) and basic operations such as insertion and searching:

```python
class TreeNode:
    def __init__(self, key):
        """Initialize a tree node with the given key."""
        self.left = None  # Left child
        self.right = None  # Right child
        self.value = key  # Value of the node

class BinarySearchTree:
    def __init__(self):
        """Initialize an empty Binary Search Tree."""
        self.root = None

    def insert(self, key):
        """Insert a new key into the BST."""
        if self.root is None:
            self.root = TreeNode(key)  # Create root node if tree is empty
        else:
            self._insert_recursive(self.root, key)

    def _insert_recursive(self, node, key):
        """Helper method to insert a key recursively."""
        if key < node.value:  # If key is less than current node's value
            if node.left is None:
                node.left = TreeNode(key)  # Insert as left child
            else:
                self._insert_recursive(node.left, key)  # Recur on left subtree
        else:  # If key is greater than or equal to current node's value
            if node.right is None:
                node.right = TreeNode(key)  # Insert as right child
            else:
                self._insert_recursive(node.right, key)  # Recur on right subtree

    def search(self, key):
        """Search for a key in the BST."""
        return self._search_recursive(self.root, key)

    def _search_recursive(self, node, key):
        """Helper method to search for a key recursively."""
        if node is None or node.value == key:  # Base case: found or reached leaf
            return node
        if key < node.value:
            return self._search_recursive(node.left, key)  # Search left subtree
        return self._search_recursive(node.right, key)  # Search right subtree

# Example usage:
bst = BinarySearchTree()
bst.insert(15)
bst.insert(10)
bst.insert(20)
bst.insert(8)
bst.insert(12)

# Searching for a value in the BST
result = bst.search(10)
if result:
    print(f"Found: {result.value}")
else:
    print("Not Found")
```

### 3. Explanation
- **TreeNode Class**: This class represents a single node in the BST. Each node contains a value and pointers to its left and right children.
- **BinarySearchTree Class**: This class manages the overall structure of the BST. It contains methods for inserting new keys and searching for existing keys.
- **Insert Method**: This method adds a new value to the BST. If the tree is empty, it creates the root node. Otherwise, it calls a helper method to find the correct position for the new value recursively.
- **Search Method**: This method checks if a specific value exists in the BST by traversing down the tree based on comparisons.

### 4. Application
In Robotics, a Binary Search Tree can be utilized to manage sensor readings efficiently. For example, when a robot collects data from multiple sensors, it can store these readings in a BST. This allows quick access to specific readings based on their timestamp or sensor ID.

In semiconductors, companies can use BSTs to organize component specifications. When engineers need to find specific components based on certain criteria (like voltage or power rating), they can do so efficiently with a BST.

In consumer electronics, a BST can be used in product catalogs. When users search for products based on their specifications or features, the BST allows for fast retrieval of relevant products.

### Integration
This content provides a structured approach to learning about Binary Search Trees while connecting it to practical applications relevant to your interests in Robotics, semiconductors, and consumer electronics. The hands-on code examples and explanations are designed to enhance your understanding and mastery of DSA fundamentals.

Stay engaged with project-based learning and apply these concepts in real-world scenarios to solidify your knowledge!