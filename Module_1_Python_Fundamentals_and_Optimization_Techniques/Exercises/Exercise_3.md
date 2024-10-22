### Module Title: Python Fundamentals and Optimization Techniques

### Exercise Requirements

1. **Problem Statement**: 
   You are tasked with developing a memory-efficient algorithm to calculate the ingredients needed for making pizzas based on the number of pizzas ordered during a Chelsea F.C. match day. The program should take into account the number of different pizza types ordered and their respective ingredient requirements. Use control flow statements to determine if you have enough ingredients available and to adjust the quantities accordingly.

   For example, if 10 Margherita pizzas and 5 Pepperoni pizzas are ordered, the program should calculate the total amount of ingredients needed and check if the stock is sufficient. If not, it should print a message indicating which ingredient is lacking.

2. **Fill-in-the-Blank Starter Code**:
```python
# Starter code for implementing pizza ingredient calculations
def calculate_ingredients(pizza_orders):
    # Define the ingredient requirements for each type of pizza
    ingredient_requirements = {
        'Margherita': {'cheese': 100, 'tomato_sauce': 50},
        'Pepperoni': {'cheese': 120, 'tomato_sauce': 50, 'pepperoni': 30}
    }
    
    # Initialize total ingredients needed
    total_ingredients = {'cheese': 0, 'tomato_sauce': 0, 'pepperoni': 0}
    
    # Loop through each pizza order
    for pizza_type, quantity in pizza_orders.items():
        # Check if the pizza type is in the requirements
        if pizza_type in ingredient_requirements:
            # Calculate total ingredients for this pizza type
            for ingredient, amount in ingredient_requirements[pizza_type].items():
                total_ingredients[ingredient] += amount * quantity
    
    # Check ingredient availability
    available_ingredients = {'cheese': 1000, 'tomato_sauce': 500, 'pepperoni': 300}  # Example stock
    for ingredient, required in total_ingredients.items():
        if required > available_ingredients[ingredient]:
            print(f"Not enough {ingredient} available! Need {required}, but have {available_ingredients[ingredient]}.")
        else:
            print(f"Sufficient {ingredient} available for {pizza_type} pizzas.")
    
    return total_ingredients

# Test the function with example orders
pizza_orders = {
    'Margherita': 10,
    'Pepperoni': 5
}
calculate_ingredients(pizza_orders)
```

3. **Hints**:
   - Remember to use loops to iterate over the orders and conditionals to check against the available ingredients.
   - Consider using a dictionary to store both the ingredient requirements and the total ingredients needed.
   - Ensure that you check each ingredient against its availability after calculating the totals.

4. **Expected Outcome**:
   The student should fill in the blanks correctly, demonstrating an understanding of how to implement control flow using conditionals and loops in Python. The final solution should include proper checks for each ingredient's availability and print appropriate messages based on whether the stock is sufficient or not. The code should be well-commented to explain the reasoning behind each step, adhering to best practices in programming.

### Integration
- Ensure that this exercise is formatted clearly with headings and sections for easy parsing and integration into your learning platform.
- Use markdown for formatting and include any necessary links or resources that may assist in completing the exercise. 

This exercise aligns with your interests in data analysis and automation while incorporating a practical application related to your passion for cooking and Chelsea F.C. It also reinforces key concepts from the lecture on control flow and optimization techniques in Python.