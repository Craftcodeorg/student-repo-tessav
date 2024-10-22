### Module Title: Data Structures and Algorithms (DSA)

### Exercise Requirements

1. **Problem Statement**:  
   You are tasked with creating a binary tree to store player performance metrics for Chelsea F.C. This binary tree should allow for efficient searching, insertion, and traversal of player statistics such as goals scored, assists, and matches played. The binary tree should be structured such that each node represents a player, and the left child of a node contains players with fewer goals than the parent node, while the right child contains players with more goals. This will help in efficiently querying player performance based on their goal-scoring capabilities.

2. **Fill-in-the-Blank Starter Code**:  
   Below is a starter code snippet that you will need to complete. Fill in the blanks to implement the functionality of the binary tree for storing player metrics.

   ```python
   class PlayerNode:
       def __init__(self, name, goals, assists, matches):
           self.name = name  # Player's name
           self.goals = goals  # Goals scored
           self.assists = assists  # Assists made
           self.matches = matches  # Matches played
           self.left = None  # Left child
           self.right = None  # Right child

   class PlayerBinaryTree:
       def __init__(self):
           self.root = None  # Root of the binary tree

       def insert(self, name, goals, assists, matches):
           new_player = PlayerNode(name, goals, assists, matches)
           if self.root is None:
               self.root = new_player
           else:
               self._insert_recursive(self.root, new_player)

       def _insert_recursive(self, current_node, new_player):
           if new_player.goals < current_node.goals:
               if current_node.left is None:
                   current_node.left = new_player
               else:
                   self._insert_recursive(current_node.left, new_player)
           else:
               if current_node.right is None:
                   current_node.right = new_player
               else:
                   self._insert_recursive(current_node.right, new_player)

       def display_in_order(self, node):
           if node is not None:
               self.display_in_order(node.left)
               print(f"Player: {node.name}, Goals: {node.goals}, Assists: {node.assists}, Matches: {node.matches}")
               self.display_in_order(node.right)

   # Example usage
   chelsea_team = PlayerBinaryTree()
   chelsea_team.insert("Player A", _____, _____, _____)  # Fill in with metrics
   chelsea_team.insert("Player B", _____, _____, _____)  # Fill in with metrics
   chelsea_team.insert("Player C", _____, _____, _____)  # Fill in with metrics

   print("In-order display of Chelsea F.C. player metrics:")
   chelsea_team.display_in_order(chelsea_team.root)
   ```

3. **Hints**:  
   - Think about how you can structure the data for each player. What attributes will you need to represent their performance?
   - Remember that the binary tree's structure is based on the number of goals. How will this affect the placement of each player in the tree?
   - When inserting players into the tree, consider how to navigate left or right based on their goal count.
   - Use in-order traversal to display players in ascending order of their goals.

4. **Expected Outcome**:  
   By completing this exercise, you should be able to construct a binary tree that effectively stores and displays player performance metrics for Chelsea F.C. You will demonstrate an understanding of how binary trees function and how they can be used to organize data efficiently. The final solution should include error handling where necessary and be well-commented to explain the reasoning behind each step.

### Integration

- Ensure that the exercise content is well-structured with clear headings and sections for easy parsing and integration into the learning platform. Use markdown for formatting.
- Include any necessary files or resources as links for further reading or reference.
- This exercise aligns with your interests in data analysis and artificial intelligence by applying data structures to real-world scenarios in sports analytics.