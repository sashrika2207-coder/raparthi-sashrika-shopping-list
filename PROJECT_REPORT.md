# 🛒 SMART SHOPPING LIST SYSTEM
## 📋 A Comprehensive Project Report

---

## 1️⃣ TITLE
### **🛍️ Smart Shopping List Management System**

> A Python-based application to manage shopping items, track prices, quantities, and calculate bills efficiently.

---

## 2️⃣ AIM OF THE PROJECT

The main aim of this project is to:
- ✅ Create a simple and user-friendly system to manage shopping items
- ✅ Keep track of prices and quantities of purchased items
- ✅ Maintain an organized shopping list with real-time updates
- ✅ Calculate itemized bills and grand totals automatically
- ✅ Reduce manual calculations and prevent mathematical errors
- ✅ Help users manage household and business shopping expenses efficiently

---

## 3️⃣ INTRODUCTION

Shopping is an everyday activity for everyone. Whether it's household groceries, office supplies, or retail products, managing a shopping list manually can be tedious and error-prone. People often forget items, lose track of prices, and make calculation mistakes while computing the final bill.

The traditional method of maintaining shopping lists on paper has several drawbacks:
- Items can be lost or forgotten
- Manual calculations are time-consuming and prone to errors
- Prices are hard to track
- No organized way to manage quantities
- Difficult to remove items once added

The **Smart Shopping List System** provides a digital solution to these problems. Built using **Python**, a beginner-friendly programming language, it allows users to easily add items, track prices, manage quantities, and automatically calculate bills without any manual computation.

This system demonstrates core programming concepts like data structures (dictionaries), user input handling, error management, and console-based interface design. It's perfect for students learning Python and practical problem-solving.

> **Suggested Image:** A person shopping with a smartphone or computer managing their shopping list

---

## 4️⃣ FEATURES OF THE PROJECT

### 🔹 A. Add Item
- Add items to the shopping list with name, price, and quantity
- Support for decimal prices (supporting currency amounts like ₹50.50)
- Store quantity as integer (whole numbers)
- Immediate confirmation message after adding item

### 🔹 B. View Shopping List
- Display all items in a formatted table
- Show columns: Item Name, Price per Unit, Quantity, Total Amount
- Calculate total amount for each item (Price × Quantity)
- Display "Shopping list is empty" message when no items are present
- Properly aligned columns for easy reading

### 🔹 C. Remove Item
- Delete specific items from the shopping list by item name
- Confirmation message when item is successfully removed
- Error message if item doesn't exist in the list
- Prevent accidental deletions with item name verification

### 🔹 D. Calculate Total Bill
- Generate itemized bill showing each item's total cost
- Display bill in organized format with items and costs
- Calculate grand total of all items
- Show summary with separator lines for clarity
- Use rupee currency format (₹) for display

### 🔹 E. User-Friendly Menu System
- Simple numbered menu with 5 clear options
- Menu repeats after each operation
- Easy navigation for users of all skill levels
- Clear visual separation between menu sections

### 🔹 F. Error Handling
- Validate price input (must be a valid float number)
- Validate quantity input (must be a valid integer)
- Handle invalid menu choices gracefully
- Display helpful error messages for user mistakes

> **Suggested Image:** Screenshot showing the shopping list menu and sample output

---

## 5️⃣ HOW THE PROJECT WORKS

### 📍 Step-by-Step Working:

**Step 1: Program Startup** 🚀
- User runs the Python program
- System initializes empty shopping list (dictionary)
- Main menu appears on the screen
- Program enters continuous loop

**Step 2: Adding Items** 📝
- User selects "Add Item" option (1)
- Enters item name (e.g., "Milk", "Bread")
- Enters price per unit as decimal number (e.g., 50.50)
- Enters quantity as integer (e.g., 2)
- System validates both price and quantity inputs
- Item is added to shopping list dictionary
- Confirmation message is displayed

**Step 3: Viewing Shopping List** 👀
- User selects "View Shopping List" option (2)
- System checks if list is empty
- If empty: displays "Shopping list is empty"
- If items exist: displays formatted table with:
  - Item names (15 character width)
  - Price per unit (10 character width, 2 decimal places)
  - Quantity (10 character width)
  - Total amount for each item (Price × Quantity)

**Step 4: Removing Items** 🗑️
- User selects "Remove Item" option (3)
- Enters the name of item to remove
- System searches for item in dictionary
- If found: deletes item and shows success message
- If not found: displays "Item not found" error message

**Step 5: Calculating Total Bill** 💰
- User selects "Calculate Total Bill" option (4)
- System displays bill summary with separator lines
- Shows each item with its total cost (Price × Quantity)
- Calculates grand total by summing all item totals
- Displays final grand total with rupee currency format

**Step 6: Exiting Program** 🔚
- User selects "Exit" option (5)
- System displays thank you message
- Program loop breaks and application closes

> **Suggested Image:** Flowchart showing the step-by-step process

---

## 6️⃣ ALGORITHM

### 🎯 Main Algorithm for Shopping List Management:

```
ALGORITHM: Smart_Shopping_List()

INPUT: User choices and item details
OUTPUT: Updated shopping list and calculated bills

BEGIN
    1. Initialize empty dictionary called "shopping_list"
    
    2. REPEAT:
        a. Display main menu with 5 options
        
        b. Get user choice (1-5)
        
        c. SWITCH choice:
        
            CASE 1 (Add Item):
                i. Get item name from user
                ii. TRY:
                    - Get price (convert to float)
                    - Get quantity (convert to int)
                    - IF conversion successful:
                        * Store in shopping_list[item_name] = {"price": price, "quantity": quantity}
                        * Display "Item added successfully"
                    - ELSE:
                        * Display "Invalid input! Please enter numbers"
                iii. END TRY
            
            CASE 2 (View List):
                i. IF shopping_list is empty:
                    - Display "Shopping list is empty"
                ii. ELSE:
                    - Print table header (Item, Price, Qty, Total)
                    - FOR each item in shopping_list:
                        * Calculate total = price × quantity
                        * Display item, price, quantity, total in formatted columns
                    - END FOR
            
            CASE 3 (Remove Item):
                i. Get item name to remove
                ii. IF item exists in shopping_list:
                    - Remove item from dictionary
                    - Display "Item removed successfully"
                iii. ELSE:
                    - Display "Item not found"
            
            CASE 4 (Calculate Bill):
                i. Initialize grand_total = 0
                ii. Display bill summary header
                iii. FOR each item in shopping_list:
                    - Calculate item_total = price × quantity
                    - Add item_total to grand_total
                    - Display item name with item_total
                iv. END FOR
                v. Display separator line
                vi. Display "Grand Total = ₹grand_total" (formatted to 2 decimal places)
            
            CASE 5 (Exit):
                i. Display thank you message
                ii. Break from loop
            
            DEFAULT:
                i. Display "Invalid choice! Please try again"
        
        d. END SWITCH
        
    3. UNTIL user chooses exit (option 5)
    
    4. Program ends
    
END
```

### 🎯 Algorithm for Price and Quantity Validation:

```
ALGORITHM: Validate_Input()

INPUT: Price and Quantity from user
OUTPUT: Validated numeric values or error message

BEGIN
    1. Get price_input as string from user
    
    2. Get quantity_input as string from user
    
    3. TRY:
        a. Convert price_input to float
            - IF conversion fails: raise ValueError
            - ELSE: price = converted float value
        
        b. Convert quantity_input to int
            - IF conversion fails: raise ValueError
            - ELSE: quantity = converted int value
        
        c. IF both conversions successful:
            - Return (price, quantity, True)
            - Status: Input is valid
    
    4. CATCH ValueError exception:
        a. Display error message: "Invalid input! Please enter numbers"
        b. Return (None, None, False)
        c. Status: Input is invalid
    
    5. END TRY-CATCH

END
```

> **Suggested Image:** Flowchart diagram of the algorithms

---

## 7️⃣ PYTHON SOURCE CODE EXPLANATION

### 💻 Core Components:

#### A. Data Structure - Shopping List Dictionary
```python
shopping_list = {}
```
**Explanation:** 
- Dictionary is used to store items with their properties
- Key: item name (string)
- Value: another dictionary with "price" and "quantity"
- Example structure: `{"Milk": {"price": 50.0, "quantity": 2}, "Bread": {"price": 30.0, "quantity": 1}}`

#### B. Main Menu Loop
```python
while True:
    print("\n===== SMART SHOPPING LIST =====")
    print("1. Add Item")
    print("2. View Shopping List")
    print("3. Remove Item")
    print("4. Calculate Total Bill")
    print("5. Exit")
    
    choice = input("Enter your choice: ")
```
