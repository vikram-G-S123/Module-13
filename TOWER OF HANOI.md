# Exp.No:35  
## TOWER OF HANOI

---

### AIM  
To write a Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user.

---

### ALGORITHM  

1. **Start the program.**
2. **Input** the number of disks `n`.
3. **Print** the number of disks.
4. Define a **recursive function** `TowerOfHanoi(n, source, destination, auxiliary)`:
   - If `n == 1`:
     - Print: "Move disk from source to destination".
   - Else:
     - Call `TowerOfHanoi(n - 1, source, auxiliary, destination)`  
       → Move `n-1` disks from source to auxiliary using destination as helper.
     - Print: "Move disk from source to destination"  
       → Move the largest disk to the destination.
     - Call `TowerOfHanoi(n - 1, auxiliary, destination, source)`  
       → Move `n-1` disks from auxiliary to destination using source as helper.
5. Call `TowerOfHanoi(n, 'A', 'C', 'B')` to start the process.
6. **End the program.**

---

### PROGRAM  

```
# Name: Vikram GS
# Reg No: 212222060296

def hanoi(n, source, temp, dest):
    if n == 1:
        print("Move disk 1 from", source, "to", dest)
        return
    hanoi(n-1, source, dest, temp)
    print("Move disk", n, "from", source, "to", dest)
    hanoi(n-1, temp, source, dest)

n = int(input("Enter number of disks: "))
hanoi(n, 'A', 'B', 'C')

```

### OUTPUT

Enter number of disks: 3
Move disk 1 from A to C
Move disk 2 from A to B
Move disk 1 from C to B
Move disk 3 from A to C
Move disk 1 from B to A
Move disk 2 from B to C
Move disk 1 from A to C



### RESULT

Tower of Hanoi problem is solved successfully using recursion.
