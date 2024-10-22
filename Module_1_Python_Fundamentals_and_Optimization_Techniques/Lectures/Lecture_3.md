# Lecture: 3. Control Flow: Conditionals and Loops

## 1. Learning Objectives:
By the end of this lecture, learners will be able to:
- Understand and implement conditional statements (if, elif, else) to control the flow of their Python programs.
- Utilize loops (for and while) to perform repetitive tasks efficiently.
- Apply these control flow concepts in practical scenarios, particularly in data analysis and AI applications relevant to the sports industry.

## 2. Introduction:
Control flow is a fundamental aspect of programming that dictates how a program executes instructions based on certain conditions. Understanding control flow is crucial for mastering data structures and algorithms (DSA), as it allows for the creation of dynamic and responsive programs.

In the context of your interests, think of control flow like a soccer match strategy: just as a coach decides whether to attack or defend based on the game situation, programmers use conditionals to determine which code to execute. Mastering these concepts will help you optimize your Python code, making it more efficient—much like a well-planned play that leads Chelsea F.C. to victory!

## 3. Core Concepts:

### A. Conditionals
- **If Statement**: Executes a block of code if a specified condition is true.
  ```python
  score = 3
  if score > 2:
      print("Chelsea wins!")
  ```

- **Elif and Else**: Allow for multiple conditions to be checked sequentially.
  ```python
  score = 1
  if score > 2:
      print("Chelsea wins!")
  elif score == 2:
      print("It's a draw!")
  else:
      print("Chelsea loses!")
  ```

### B. Loops
- **For Loop**: Iterates over a sequence (like a list or range).
  ```python
  for player in ["Sterling", "Havertz", "Mount"]:
      print(player + " is on the field.")
  ```

- **While Loop**: Continues to execute as long as a condition remains true.
  ```python
  goals = 0
  while goals < 3:
      goals += 1
      print("Goal scored! Total goals: " + str(goals))
  ```

## 4. Practical Application:
In the world of Premier League Soccer, data analysis plays a significant role in team strategy. For example, using conditionals, analysts can evaluate player performance metrics and decide which players should be on the field based on their stats.

### Example Scenario:
Imagine you are developing a simple program that analyzes player performance:
```python
player_stats = {'goals': 3, 'assists': 1}

if player_stats['goals'] > 2:
    print("Player is performing excellently!")
elif player_stats['goals'] == 2:
    print("Player is performing well.")
else:
    print("Player needs improvement.")
```
This code snippet evaluates player stats and provides feedback, similar to how coaches assess players based on match performance.

## 5. Summary:
In this lecture, we explored control flow using conditionals and loops. You learned how to use if statements to make decisions in your code and how loops can help automate repetitive tasks. These skills are essential for optimizing your code and applying data structures effectively.

## 6. Next Steps:
In our next lecture, we will delve into functions in Python—an essential building block for writing clean, reusable code. To prepare, review the concepts of conditionals and loops and think about how you might use functions to encapsulate the logic you've learned today. This will set you up for success as we explore more advanced topics in Python programming!