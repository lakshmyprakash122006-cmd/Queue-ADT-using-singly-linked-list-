# Queue-ADT-using-singly-linked-list-
Data structure practical program 
# Queue using Singly Linked List

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

front = None
rear = None

# Enqueue operation
def enqueue():
    global front, rear
    x = int(input("Enter element: "))
    newnode = Node(x)

    if rear is None:
        front = rear = newnode
    else:
        rear.next = newnode
        rear = newnode

# Dequeue operation
def dequeue():
    global front, rear
    if front is None:
        print("Queue is empty")
    else:
        print("Deleted element:", front.data)
        front = front.next
        if front is None:
            rear = None

# Display queue
def display():
    temp = front
    if temp is None:
        print("Queue is empty")
    else:
        while temp:
            print(temp.data, end=" ")
            temp = temp.next
        print()

while True:
    print("\n1.Enqueue 2.Dequeue 3.Display 4.Exit")
    ch = int(input("Enter choice: "))

    if ch == 1:
        enqueue()
    elif ch == 2:
        dequeue()
    elif ch == 3:
        display()
    elif ch == 4:
        break
    else:
        print("Invalid choice")
  output:
  1.Enqueue 2.Dequeue 3.Display 4.Exit
Enter choice: 1
Enter element: 10

Enter choice: 1
Enter element: 20

Enter choice: 3
10 20

Enter choice: 2
Deleted element: 10
