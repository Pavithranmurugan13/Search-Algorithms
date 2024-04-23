# Linear Search and Binary search

## Aim:

To write a program to perform linear search and binary search using python programming.

## Equipment’s required:

1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

## Linear Search:

1. Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2. If k matches with an element in array[] , return the index.
3. If k doesn’t match with any of elements in array[], return -1 or element not found.

## Binary Search:

1. Set two pointers low and high at the lowest and the highest positions respectively.
2. Find the middle element mid of the array ie. arr[(low + high)/2]
3. If x == mid, then return mid.Else, compare the element to be searched with m.
4. If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5. Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6. Repeat steps 2 to 5 until low meets high

## Program:

i) #Use a linear search method to match the item in a list.

```python
#commond line for linear search
#name:PAVITHRAN M J
#reg no:212223240112

def search(array,key,n):
    for i in range (0,n):
        if key==array[i]:
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
    
```

ii) # Find the element in a list using Binary Search(Iterative Method).

```python
#commond line for binary search
#name:PAVITHRAN M J
#reg no:212223240112

def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array [mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```

iii) # Find the element in a list using Binary Search (recursive Method).

```python
#commond line for binary search
#name:PAVITHRAN M J
#reg no:212223240112

def binary(array,key,low,high):
    if(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array [mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```

## Sample Input and Output

i) #Use a linear search method to match the item in a list.
![Screenshot 2024-04-23 110023](https://github.com/Pavithranmurugan13/Search-Algorithms/assets/163802201/35be5aef-febc-4f4d-8fe0-89977b2ed791)

ii) # Find the element in a list using Binary Search(Iterative Method).
![Screenshot 2024-04-23 110043](https://github.com/Pavithranmurugan13/Search-Algorithms/assets/163802201/ba8e4f9a-5d57-4e62-8307-a6651eddadd5)


iii) # Find the element in a list using Binary Search (recursive Method).
![Screenshot 2024-04-23 110103](https://github.com/Pavithranmurugan13/Search-Algorithms/assets/163802201/382bc726-7dfc-4bfd-acc8-318666502884)



## Result

Thus the linear search and binary search algorithm is implemented using python programming.
