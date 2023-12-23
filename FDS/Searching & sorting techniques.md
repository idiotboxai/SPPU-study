## Unit III: Searching and Sorting (06 Hours)

- [x]  Sequential Search/Linear Search
- [x]  Variant of Sequential Search - Sentinel Search
- [x]  Binary Search
 
- [x]  Indexed Sequential Search
- [x]  Types of Sorting (Internal and External)
- [ ]  General Sort Concepts (Sort Order, Stability, Efficiency, Number of Passes)
- [ ]  Comparison-Based Sorting Methods
    - [ ]  Bubble Sort
    - [ ]  Insertion Sort
    - [ ]  Selection Sort
    - [ ]  Quick Sort
    - [ ]  Shell Sort
- [ ]  Non-comparison Based Sorting Methods
    - [ ]  Radix Sort
    - [ ]  Counting Sort
    - [ ]  Bucket Sort
- [ ]  Comparison of All Sorting Methods and Their Complexities

## Unit IV: Linked List (07 Hours)

- [ ]  Introduction to Static and Dynamic Memory Allocation
- [ ]  Linked List Introduction
- [ ]  Realization of Linked List using Dynamic Memory Management
- [ ]  Operations on Linked List
- [ ]  Linked List as ADT
- [ ]  Types of Linked List
    - [ ]  Singly Linked List
    - [ ]  Linear Linked List
    - [ ]  Circular Linked List
    - [ ]  Doubly Linked List
    - [ ]  Doubly Circular Linked List
- [ ]  Primitive Operations on Linked List
    - [ ]  Create
    - [ ]  Traverse
    - [ ]  Search
    - [ ]  Insert
    - [ ]  Delete
    - [ ]  Sort
    - [ ]  Concatenate
- [ ]  Polynomial Manipulations - Polynomial Addition
- [ ]  Generalized Linked List (GLL) Concept
- [ ]  Representation of Polynomial using GLL

## Unit V: Stack (07 Hours)

- [ ]  Basic Concept
- [ ]  Stack Abstract Data Type
- [ ]  Representation of Stacks Using Sequential Organization
- [ ]  Stack Operations
- [ ]  Multiple Stacks
- [ ]  Applications of Stack
    - [ ]  Expression Evaluation and Conversion
    - [ ]  Polish Notation and Expression Conversion
    - [ ]  Need for Prefix and Postfix Expressions
    - [ ]  Postfix Expression Evaluation
- [ ]  Linked Stack and Operations
- [ ]  Recursion Concept
- [ ]  Variants of Recursion
    - [ ]  Direct Recursion
    - [ ]  Indirect Recursion
    - [ ]  Tail Recursion
    - [ ]  Tree Recursion
- [ ]  Backtracking Algorithmic Strategy
- [ ]  Use of Stack in Backtracking

## Unit VI: Queue (06 Hours)

- [ ]  Basic Concept
- [ ]  Queue as Abstract Data Type
- [ ]  Representation of Queue using Sequential Organization
- [ ]  Queue Operations
- [ ]  Circular Queue and Its Advantages
- [ ]  Multi-Queues
- [ ]  Linked Queue and Operations
- [ ]  Deque Basic Concept
- [ ]  Types of Deque (Input Restricted and Output Restricted)
- [ ]  Priority Queue Basic Concept
- [ ]  Types of Priority Queue (Ascending and Descending)
      

# Searching and Sorting 

## **Linear Search**

Linear search is a very simple search algorithm. In this type of search, a sequential search is made over all items one by one. Every item is checked and if a match is found then that particular item is returned, otherwise the search continues till the end of the data collection.

![[linear_search.gif]]

This is this the simple algorithm for understanding and helpful for small data
Linear Search (Array A, Value x)

#### Algorithm

Linear Search ( Array A, Value x)

Step 1: Set i to 1
Step 2: if i > n then go to step 7
Step 3: if A[i] = x then go to step 6
Step 4: Set i to i + 1
Step 5: Go to Step 2
Step 6: Print Element x Found at index i and go to step 8
Step 7: Print element not found
Step 8: Exit

#### Pseudocode

procedure linear_search (list, value)
``
   `for each item in the list
     `` if match item == value
       ``  return the item's location
      `end if
   `end for
`end procedure

---

## **Binary Search**

Binary Search is a searching algorithm for finding an element's position in a sorted array.

In this approach, the element is always searched in the middle of a portion of an array.

`Binary search can be implemented only on a sorted list of items. If the elements are not sorted already, we need to sort them first.



#### Binary Search Working

Binary Search Algorithm can be implemented in two ways which are discussed below.

1. Iterative Method
2. Recursive Method

The recursive method follows [the divide and conquer](https://www.programiz.com/dsa/divide-and-conquer) approach.

The general steps for both methods are discussed below.

1. The array in which searching is to be performed is:
    
    ![initial array Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-initial-array.png "initial array")
    
    Initial array
    
      
    Let `x = 4` be the element to be searched.
2. Set two pointers low and high at the lowest and the highest positions respectively.
    
    ![setting pointers Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-set-pointers.png "setting pointers")
    
    Setting pointers
    
3. Find the middle element mid of the array ie. `arr[(low + high)/2] = 6`.
    
    ![mid element Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-mid.png "mid element")
    
    Mid element
    
4. If x == mid, then return mid.Else, compare the element to be searched with m.
5. If `x > mid`, compare x with the middle element of the elements on the right side of mid. This is done by setting low to `low = mid + 1`.
6. Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to `high = mid - 1`.
    
    ![finding mid element Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-find-mid.png "finding mid element")
    
    Finding mid element
    
7. Repeat steps 3 to 6 until low meets high.
    
    ![mid element Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-mid-again.png "mid element")
    
    Mid element
    
8. `x = 4` is found.
    
    ![found Binary Search](https://cdn.programiz.com/sites/tutorial2program/files/binary-search-found.png "found")
    
    Found
    

#### Binary Search Algorithm

#### Iteration Method

do until the pointers low and high meet each other.
    mid = (low + high)/2
    if (x == arr[mid])
        return mid
    else if (x > arr[mid]) // x is on the right side
        low = mid + 1
    else                       // x is on the left side
        high = mid - 1

#### Recursive Method

binarySearch(arr, x, low, high)
    if low > high
        return False 
    else
        mid = (low + high) / 2 
        if x == arr[mid]
            return mid
        else if x > arr[mid]        // x is on the right side
            return binarySearch(arr, x, mid + 1, high)
        else                               // x is on the left side
            return binarySearch(arr, x, low, mid - 1)


#### Binary Search Complexity

**Time Complexities**

- **Best case complexity**: `O(1)`
- **Average case complexity**: `O(log n)`
- **Worst case complexity**: `O(log n)`

**Space Complexity**

The space complexity of the binary search is `O(1)`.

---
## Sentinel Search


Sentinel Linear Search is basically a variation of the traditional linear search algorithm. It is designed to reduce the number of comparisons required to find a specific target value within an array or list.

![[Pasted image 20231222184152.png]]

### Complexity Analysis

> **Time Complexity:** O(N)  
> **Auxiliary Space:** O(1)

### Steps

1. Append the target element (8) at the end of the array as a sentinel. Array becomes: [3, 5, 1, 8, 2, 8]
2. Initialize a loop variable **i** to 0, representing the current index.
3. Compare the element at index 0 with the target element (8). No match (**3 ≠ 8**).
4. Increment the loop variable **i** to 1 and compare the element at index 1 with the target element (8). No match (**5 ≠ 8**).
5. Increment the loop variable **i** to 2 and compare the element at index 2 with the target element (8). No match **(1 ≠ 8**).
6. Increment the loop variable **i** to 3 and compare the element at index 3 with the target element (8). A match is found (**8 = 8**).
7. The search is successful, and the **index (3)** where the match was found is returned.
   

## Indexed sentinel search
   
   In this searching method, first of all, an index file is created, that contains some specific group or division of required record when the index is obtained, then the partial indexing takes less time cause it is located in a specified group.

**Note:** When the user makes a request for specific records it will find that index group first where that specific record is recorded.

### Characteristics of Indexed Sequential Search:

- In Indexed Sequential Search a sorted index is set aside in addition to the array.
- Each element in the index points to a block of elements in the array or another expanded index.
- The index is searched 1st then the array and guides the search in the array.
  
  ### Explanation by diagram “Indexed Sequential Search”:

![](https://media.geeksforgeeks.org/wp-content/uploads/Screenshot-42-4.png)


## Sorting & its types

**`Sorting is the process of ordering or arranging a given collection of elements in some particular orde**

Sorting is the operation of arranging the records of a table
according to the key value of each record, or it can be defined
as the process of converting an unordered set of elements to an
ordered set of elements

Sorting is a process of organizing data in a certain order to help
retrieve it more efficiently

![[Pasted image 20231222193739.png]]
### Difference Between Internal and External Sort

|Internal Sort|External Sort|
|---|---|
|Internal sorting is used when the input data can be adjusted in the main memory all at once.|External sorting is used when the input data cannot be adjusted in the main memory all at once.|
|The data to be sorted should be small enough to fit in the main memory.|It is used when data to be sorted cannot fit into the main memory all at once.|
|The storage device used in this method is only main memory (RAM)|Both Secondary memory (Hard Disk) and Main memory are used in this method.|
|While sorting is in progress, all the data to be sorted is stored in the main memory at all times.|While sorting, data is loaded into the Main memory in small chunks, all data is stored outside the memory like on Hard Disk.|
|Algorithms Used for Internal Sort are Bubble sort, Insertion Sort, Quick sort, Heap sort, etc.|Algorithms Used for External Sort are Merge sort, Tape Sort, External radix sort, etc.|

## General sort concepts

1) sort order
2) stability
3) efficiency
4) pass

