# Exp.No:31  
## IMPLEMENTATION OF STACK

---

### AIM  
To write a Python program to implement a stack using a list and its built-in methods (`append()`, `pop()`).

---

### ALGORITHM

1. **Start the program.**
2. **Define a class `st`** with the following methods:
   - `push(self, num)`: Adds the number `num` to the stack.
   - `pop(self)`: Removes and returns the top element from the stack.
3. **Create a stack object `s`** using the class `st`.
4. **Input the stack size**: Take an integer input `size` to define the size of the stack.
5. **Loop through numbers from 1 to size**: Add only the odd numbers to the stack using the `push()` method.
6. **Display the elements** in the stack after the loop completes.
7. **Call `pop()`** to remove the top element from the stack and display the popped element.
8. **Display the stack again** to show the remaining elements.
9. **End the program.**

---

### PROGRAM

```

# Name: Vikram GS
# Reg No: 212222060296

stack = []

def push():
    item = input("Enter element: ")
    stack.append(item)
    print("Pushed:", item)

def pop():
    if not stack:
        print("Stack is empty")
    else:
        print("Popped:", stack.pop())

push()
push()
pop()
print("Stack:", stack)

```
**Ouput**

Enter element: 10
Pushed: 10
Enter element: 20
Pushed: 20
Popped: 20
Stack: ['10']


**Result**

Stack operations (push and pop) are performed successfully.
