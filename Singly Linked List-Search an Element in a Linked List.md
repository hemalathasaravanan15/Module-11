# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
~~~
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
 
class LinkedList:
    def __init__(self):
        self.head = None
 
    def push(self, new_data):
        new_node = Node(new_data)
        new_node.next = self.head
        self.head = new_node
 
    def search(self, x):
        current = self.head
        while current != None:
            if current.data == x:
                return True
             
            current = current.next
        return False
 
llist = LinkedList()
 
llist.push(10);
llist.push(30);
llist.push(11);
llist.push(21);
llist.push(14);

data = int(input())
if llist.search(data):
    print("Yes")
else:
    print("No")
~~~
## Sample Output
<img width="366" height="211" alt="image" src="https://github.com/user-attachments/assets/a4a9e1c7-c534-4803-8293-8ad7fc9f48c9" />


## Result
Thus the output is verified
