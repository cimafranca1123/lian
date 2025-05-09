lost_items = []

def report_item():
    item = input("What did you lose/find? ")
    location = input("Where? ")
    contact = input("Your contact info: ")
    lost_items.append({
        'item': item,
        'location': location,
        'contact': contact,
        'status': 'lost'  # or 'found'
    })
    print(f"Reported: {item} at {location}")

def show_items():
    print("\n--- Lost & Found ---")
    for i, entry in enumerate(lost_items, 1):
        print(f"{i}. {entry['item']} ({entry['status']}) at {entry['location']}")

def claim_item():
    show_items()
    try:
        num = int(input("Which item # is found/returned? ")) - 1
        if 0 <= num < len(lost_items):
            lost_items[num]['status'] = 'returned'
            print(f"Marked as returned! Contact: {lost_items[num]['contact']}")
        else:
            print("Invalid number")
    except:
        print("Please enter a number")

def main_menu():
    while True:
        print("\n=== Lost & Found ===")
        print("1. Report lost/found item")
        print("2. View all items")
        print("3. Mark as returned")
        print("4. Exit")
        
        choice = input("Choose (1-4): ")
        
        if choice == '1':
            report_item()
        elif choice == '2':
            show_items()
        elif choice == '3':
            claim_item()
        elif choice == '4':
            print("Thank you for using Lost & Found!")
            break
        else:
            print("Please choose 1-4")

# Start the system
main_menu()