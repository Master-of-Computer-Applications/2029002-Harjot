                                               Programming in Python
            
                                                  (PGCA- 207)
            

 Submitted To-:
Prof. Satinder Singh
            
                                                                                                  Submitted By-:
                                                                                                   harjot kaur
                                                                                                   MCA-2nd Sem
                                                                                                   CRN-2029002
                                                                                                   URN-2005219  

Sr no 	Experiment Name 	                                                                                                                 Remarks
1 	Write a Python program to create an array of 5 elements and display the array items Access each individual items through indexes. 	
2 	Write a Python program to reverse the order of items in the array. 	
3 	Write a Python program to append a new item to the end of the array. 	
4 	Write a Python program to remove a specified item using the index from an array. 	
5 	Write a Python program to get the length of an array. 	
6 	Write a Python program for binary Search. 	
7 	Write a Python program for sequential or linear search. 	
8 	Write a Python program to sort a list of elements using the bubble sort algorithm. 	
9 	Write a Python program to sort a list of elements using the selection sort algorithm. 	
10 	Write a Python program to sort a list of elements using the insertion sort algorithm. 	
11 	Write a Python program to sort a list of elements using the quick sort algorithm. 	
12 	Write a Python program to create a singly linked list and append some items iterate through the list. 	
13 	Write a Python program to find the size of singly linked list. 	
14 	Write a python program to search a specific item in singly linked list and return true if the item was found otherwise return false. 	
15 	Write a Python program to delete the first item from singly linked list. 	
16 	Write a Python program to create a circular linked list. 	
17 	Write a Python program to implement stack operation using list. 	
18 	Write a Python program to implement queue and its operations using list. 	
19     Write a Python program to find kth smallest element in a given binary tree.
20     Write a Python program to find kth smallest element in a given binary tree. 	
	


1. Write a Python program to create an array of 5 elements and display the array items Access each individual items through indexes:-

_Code:_
```python
import arrray as arr
a= arr.array('d',[10,20,30,40])
print(a[0])
print(a[1])
print(a[2])
print(a[3])
```
![Screenshot from 2021-06-07 19-41-46](https://user-images.githubusercontent.com/82712371/121037598-32d56100-c7cd-11eb-9cca-c354e3c10cee.png)


2. Write a Python program to reverse the order of items in the array.

_Code:_
```python
#The original array
arr = [11, 22, 33, 44, 55]
print("Before reversal Array is :",arr)
 
arr.reverse() #reversing using reverse()
print("After reversing Array:",arr)
```![Screenshot from 2021-06-07 20-18-40](https://user-images.githubusercontent.com/82712371/121038120-a7100480-c7cd-11eb-9f0a-c5872e121283.png)


3. Write a Python program to append a new item to the end of the array.

_code:_
```python
a= ['mango','orange','apple']
b= ['pear','grapes','banana']
a.append(b)
print a
```
![Screenshot from 2021-06-07 20-21-12](https://user-images.githubusercontent.com/82712371/121038426-eccccd00-c7cd-11eb-824c-1d19fc1502b0.png)


4. Write a Python program to remove a specified item using the index from an array.
_Code:_
```python
a = [1,2,3,4,5]
a.pop(1)
print"removed a specified item using the index from an array by PDP operation: ",a
```

![Screenshot from 2021-06-07 20-24-45](https://user-images.githubusercontent.com/82712371/121039109-7086b980-c7ce-11eb-8aab-86592a3ea43c.png)


5. Write a Python program to get the length of an array.
_Code_
```python
a=[1,2,3,4,'hello']
print"Display all elements:",a
print"Length of all elements: ", len(a)
```
![Screenshot from 2021-06-07 20-26-50](https://user-images.githubusercontent.com/82712371/121039440-b5125500-c7ce-11eb-84f6-b40e8c50630d.png)


6. Write a Python program for sequential or linear search.
_Code_
```python
def linearsearch(arr, x):
   for i in range(len(arr)):
      if arr[i] == x:
         return i
   return -1
arr = ['t','u','t','o','r','i','a','l']
x = 'a'
print("element found at index "+str(linearsearch(arr,x)))```
![Screenshot from 2021-06-07 20-28-54](https://user-images.githubusercontent.com/82712371/121039758-fe62a480-c7ce-11eb-91b4-4098aff13dfb.png)


7. Write a Python program for binary search.
Code:
```python
def binarySearch (arr, l, r, x):
    if r >= l:
 
        mid = l + (r - l) // 2
        if arr[mid] == x:
            return mid
        elif arr[mid] > x:
            return binarySearch(arr, l, mid-1, x)
        else:
            return binarySearch(arr, mid + 1, r, x)
    else:
        return -1
 
# Driver Code
arr = [ 2, 3, 4, 10, 40 ]
x = 10
result = binarySearch(arr, 0, len(arr)-1, x) 
if result != -1:
    print ("Element is present at index % d" % result)
else:
    print ("Element is not present in array")```![Screenshot from 2021-06-07 20-30-42](https://user-images.githubusercontent.com/82712371/121040073-41247c80-c7cf-11eb-88a5-a5b526e6402e.png)


8. Write a Python program to sort a list of elements using the bubble sort algorithm.
Code:
```python
def bubbleSort(arr):
    n = len(arr)
    for i in range(n-1):
        for j in range(0, n-i-1):
            if arr[j] > arr[j + 1] :
                arr[j], arr[j + 1] = arr[j + 1], arr[j]
arr = [64, 34, 25, 12, 22, 11, 90]
bubbleSort(arr)
print ("Sorted array is:")
for i in range(len(arr)):
    print ("% d" % arr[i]),``` ![Screenshot from 2021-06-07 20-33-27](https://user-images.githubusercontent.com/82712371/121040581-a2e4e680-c7cf-11eb-9e47-d230882008a6.png)


9. Write a Python program to sort a list of elements using the selection sort algorithm.
Code:
```python
def selectionSort(array):
  n = len(array)
  for i in range(n):
    # Initially, assume the first element of the unsorted part as the minimum.
    minimum = i

    for j in range(i+1, n):
      if (array[j] < array[minimum]):
        # Update position of minimum element if a smaller element is found.
        minimum = j

    # Swap the minimum element with the first element of the unsorted part.     
    temp = array[i]
    array[i] = array[minimum]
    array[minimum] = temp
    
  return array

# Driver code
array = [13, 4, 9, 5, 3, 16, 12]
print(selectionSort(array))
```![Screenshot from 2021-06-07 20-34-47](https://user-images.githubusercontent.com/82712371/121040799-d32c8500-c7cf-11eb-84da-882f2d6a677d.png)


10. Write a Python program to sort a list of elements using the insertion sort algorithm.
Code:
```python
def insertionSort(arr):
  
    # Traverse through 1 to len(arr)
    for i in range(1, len(arr)):
  
        key = arr[i]
  
        # Move elements of arr[0..i-1], that are
        # greater than key, to one position ahead
        # of their current position
        j = i-1
        while j >=0 and key < arr[j] :
                arr[j+1] = arr[j]
                j -= 1
        arr[j+1] = key
  
  
# Driver code to test above
arr = [12, 11, 13, 5, 6]
insertionSort(arr)
print ("Sorted array is:")
for i in range(len(arr))
    print ("%d" %arr[i])```![Screenshot from 2021-06-07 20-36-18](https://user-images.githubusercontent.com/82712371/121041054-08d16e00-c7d0-11eb-8b74-d0c9223e7857.png)


11. Write a Python program to sort a list of elements using the quick sort algorithm.

Code:
```python

def partition(arr, low, high):
	i = (low-1)		 # index of smaller element
	pivot = arr[high]	 # pivot
	for j in range(low, high):
		if arr[j] <= pivot:
			i = i+1
			arr[i], arr[j] = arr[j], arr[i]
	arr[i+1], arr[high] = arr[high], arr[i+1]
	return (i+1)
def quickSort(arr, low, high):
	if len(arr) == 1:
		return arr
	if low < high:
		pi = partition(arr, low, high)
		quickSort(arr, low, pi-1)
		quickSort(arr, pi+1, high)
arr = [10, 7, 8, 9, 1, 5]
n = len(arr)
quickSort(arr, 0, n-1)
print("Sorted array is:")
for i in range(n):
	print("%d" % arr[i])
	```

![Screenshot from 2021-06-07 20-37-34](https://user-images.githubusercontent.com/82712371/121041243-34545880-c7d0-11eb-97d6-495c189e483b.png)


12. Write a Python program to create a singly linked list and append some items iterate through the list.

Code:
```python
class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.head = None
        self.tail = None
        self.count = 0
    def iterate_item(self):
        # Iterate the list.
        current_item = self.head
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val
    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.tail:
            self.tail.next = node
            self.tail = node
        else:
            self.head = node
            self.tail = node
        self.count += 1
items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')
for val in items.iterate_item():
    print(val)
print("\nhead.data: ",items.head.data)
print("tail.data: ",items.tail.data)
```![Screenshot from 2021-06-07 20-39-27](https://user-images.githubusercontent.com/82712371/121041811-b775ae80-c7d0-11eb-9996-025f4f863a6b.png)


13. Write a Python program to find the size of singly linked list.

Code:
```python
class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0
	
    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1
    
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print "Original list:"
for val in items.iterate_item():
    print(val)

print "Size of the list:",items.count
```![Screenshot from 2021-06-07 20-42-43](https://user-images.githubusercontent.com/82712371/121042044-eee45b00-c7d0-11eb-8a4d-b43e7a7cc071.png)


14. Write a python program to search a specific item in singly linked list and return true if the item was found otherwise return false.

Code:
```python
class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1
    
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

    def search_item(self, val):
         # Search the list
         for node in self.iterate_item():
             if val == node:
                 return True
         return False

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

if items.search_item('SQL'):
    print("True")
else:
    print("False")

if items.search_item('C++'):
    print("True")
else:
    print("False")
    ```![Screenshot from 2021-06-07 20-44-16](https://user-images.githubusercontent.com/82712371/121042277-25ba7100-c7d1-11eb-9a3a-36a86571b70c.png)


15. Write a Python program to delete the first item from singly linked list.

Code:
```python

class Node:
    # Singly linked node
    def __init__(self, data=None):
        self.data = data
        self.next = None
class singly_linked_list:
    def __init__(self):
        # Createe an empty list
        self.tail = None
        self.head = None
        self.count = 0

    def append_item(self, data):
        #Append items on the list
        node = Node(data)
        if self.head:
            self.head.next = node
            self.head = node
        else:
            self.tail = node
            self.head = node
        self.count += 1
    
    def delete_item(self, data):
        # Delete an item from the list
        current = self.tail
        prev = self.tail
        while current:
            if current.data == data:
                if current == self.tail:
                    self.tail = current.next
                else:
                    prev.next = current.next
                self.count -= 1
                return
            prev = current
            current = current.next
    def iterate_item(self):
        # Iterate the list.
        current_item = self.tail
        while current_item:
            val = current_item.data
            current_item = current_item.next
            yield val

items = singly_linked_list()
items.append_item('PHP')
items.append_item('Python')
items.append_item('C#')
items.append_item('C++')
items.append_item('Java')

print("Original list:")
for val in items.iterate_item():
    print(val)

print("\nAfter removing the first item from the list:")
items.delete_item('PHP')
for val in items.iterate_item():
    print(val)
    ```![Screenshot from 2021-06-07 20-45-40](https://user-images.githubusercontent.com/82712371/121042466-58646980-c7d1-11eb-9de4-e87055c946a5.png)


16. Write a Python program to create a circular linked list.

Code:
```python

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class CircularLinkedList:
    def __init__(self):
        self.head = None
    def push(self, data):
        ptr1 = Node(data)
        temp = self.head
        ptr1.next = self.head
        if self.head is not None:
            while(temp.next != self.head):
                temp = temp.next
            temp.next = ptr1 
        else:
            ptr1.next = ptr1 # For the first node
        self.head = ptr1
    def printList(self):
        temp = self.head
        if self.head is not None:
            while(True):
                print "%d" %(temp.data),
                temp = temp.next
                if (temp == self.head):
                    break
cllist = CircularLinkedList()
cllist.push(12)
cllist.push(56)
cllist.push(2)
cllist.push(11)
 
print "Contents of circular Linked List"
cllist.printList()```![Screenshot from 2021-06-07 20-47-06](https://user-images.githubusercontent.com/82712371/121042672-8a75cb80-c7d1-11eb-9931-74e488e921bb.png)


17. Write a Python program to implement stack operation using list.

Code:
```python

stack = []
 
# append() function to push
# element in the stack
stack.append('a')
stack.append('b')
stack.append('c')
 
print "Initial stack"
print(stack)
 
# pop() fucntion to pop
# element from stack in
# LIFO order
print "Elements poped from stack:"
print(stack.pop())
print(stack.pop())
print(stack.pop())
 
print "nStack after elements are poped:"
print stack
```![Screenshot from 2021-06-07 20-48-20](https://user-images.githubusercontent.com/82712371/121042872-b6914c80-c7d1-11eb-8600-05b0c504c46d.png)


18. Write a Python program to implement queue and its operations using list.

Code:
```python

queue = []
queue.append('a')
queue.append('b')
queue.append('c')
print "Initial queue"
print queue
print "Elements dequeued from queue"
print(queue.pop(0))
print(queue.pop(0))
print(queue.pop(0)) 
print"Queue after removing elements"
print queue
```![Screenshot from 2021-06-07 20-49-23](https://user-images.githubusercontent.com/82712371/121042995-db85bf80-c7d1-11eb-887e-42ef5317a89e.png)


19. Write a Python program to count the number of nodes in binary search tree.

Code:
```python

class Node:
    def __init__(self ,key):
        self.data = key
        self.left = None
        self.right = None
def getfullCount(root):
    if root is None:
        return 0
    queue = []
    queue.append(root)       
    count = 0 #initialize count for full nodes
    while(len(queue) > 0):
        node = queue.pop(0)
        if node.left is not None and node.right is not None:
            count = count+1
        if node.left is not None:
            queue.append(node.left)
        if node.right is not None:
            queue.append(node.right)     
    return count
root = Node(2)
root.left = Node(7)
root.right = Node(5)
root.left.right = Node(6)
root.left.right.left = Node(1)
root.left.right.right = Node(11)
root.right.right = Node(9)
root.right.right.left = Node(4) 
print "%d" %(getfullCount(root))
```![Screenshot from 2021-06-07 20-50-55](https://user-images.githubusercontent.com/82712371/121043250-12f46c00-c7d2-11eb-9ed4-8ef59a837dd8.png)


20. Write a Python program to find kth smallest element in a given binary tree.

Code:
```python

class TreeNode(object):
    def __init__(self, x):
        self.val = x
        self.left = None
        self.right = None

def kth_smallest(root, k):
    stack = []
    while root or stack:
        while root:
            stack.append(root)
            root = root.left
        root = stack.pop()
        k -= 1
        if k == 0:
            break
        root = root.right
    return root.val

root = TreeNode(8)  
root.left = TreeNode(5)  
root.right = TreeNode(14) 
root.left.left = TreeNode(4)  
root.left.right = TreeNode(6) 
root.left.right.left = TreeNode(8)  
root.left.right.right = TreeNode(7)  
root.right.right = TreeNode(24) 
root.right.right.left = TreeNode(22)  

print(kth_smallest(root, 2))
print(kth_smallest(root, 3))
```![Screenshot from 2021-06-07 20-52-41](https://user-images.githubusercontent.com/82712371/121043501-5222bd00-c7d2-11eb-92a1-544174cf7ec6.png)


