# Shopping Cart using List

cart = []

def add_item():
    item = input("Enter item name: ")
    price = float(input("Enter item price: "))
    quantity = int(input("Enter quantity: "))
    cart.append([item, price, quantity])
    print("Item added to cart")

def remove_item():
    item = input("Enter item name to remove: ")
    for i in cart:
        if i[0] == item:
            cart.remove(i)
            print("Item removed")
            return
    print("Item not found")

def display_cart():
    total = 0
    print("\nItems in Cart:")
    for item, price, quantity in cart:
        cost = price * quantity
        total += cost
        print(item, "- Price:", price, "Qty:", quantity, "Cost:", cost)
    print("Total Bill:", total)


while True:
    print("\n1.Add Item  2.Remove Item  3.Display Cart  4.Exit")
    choice = int(input("Enter choice: "))

    if choice == 1:
        add_item()
    elif choice == 2:
        remove_item()
    elif choice == 3:
        display_cart()
    elif choice == 4:
        break
    else:
        print("Invalid choice")# Data-structure-practical-program37
