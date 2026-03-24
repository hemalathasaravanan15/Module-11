# 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
~~~
class Node:
    def __init__(self, value):
        self.data = value
        self.next = None
      
class LinkedList:
  
    def __init__(self):
        self.head = None
  
    def push(self, new_data):
        new_node = Node(new_data)
        new_node.next = self.head
        self.head = new_node
          
    def printMiddle(self):
        temp = self.head 
        count = 0
          
        while self.head:
            if (count & 1): 
                temp = temp.next
            self.head = self.head.next
            count += 1 
          
        print(temp.data)     
          
llist = LinkedList() 
for i in range(5):
    value = input()
    llist.push(value)

llist.printMiddle()
~~~

## Sample Input & Output
<img width="412" height="254" alt="image" src="https://github.com/user-attachments/assets/d07cea19-63ec-4f70-b8e8-5565f7ecdddc" />


## Result
Thuds the desired output is verified.
