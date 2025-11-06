# python_hotel.py

# Define menu (example items with prices)
menu = {
    "Pizza": 150,
    "Burger": 80,
    "Pasta": 120,
    "Coffee": 50
}

# Initialize total
order_total = 0

# First order
item_1 = input("Enter the name of item you want to order = ")
if item_1 in menu:
    order_total += menu[item_1]  # 0 + price of item_1
    print(f"Your item {item_1} has been added to your order")

else:
    print(f"Ordered item {item_1} is not available yet")

# Ask if another item is needed
another_order = input("Do you want to add another item ? (Yes/No) ")
if another_order.lower() == "yes":
    item_2 = input("Enter the name of second item = ")
    if item_2 in menu:
        order_total += menu[item_2]
        print(f"Item {item_2} has been added to order")
    else:
        print(f"Ordered item {item_2} is not available!")

# Final bill
print(f"The total amount of items to pay is {order_total}")
