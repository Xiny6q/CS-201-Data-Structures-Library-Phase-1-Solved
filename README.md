Download link :https://programming.engineering/product/cs-201-data-structures-library-phase-1-solved/

# CS-201-Data-Structures-Library-Phase-1-Solved
CS 201 Data Structures Library Phase 1 Solved
For phase 1 of the CS201 programming project, we will start with a dynamic array class and extend it to implement some of the algorithms discussed in class.

Your dynamic array class should be called CircularDynamicArray. The CircularDynamicArray class should manage the storage of an array that can grow and shrink. The class should be implemented using templates. As items are added and removed from both the front and the end of the array, the items will always be referenced using indices 0…size-1.

The public methods of your class should include the following (elmtype indicates the type from the template):

Function

Description

Runtime

CircularDynamicArray();

Default Constructor. The array should be of capacity 2.

O(1)

CircularDynamicArray(int s);

For this constructor the array should be of capacity and

O(1)

size s.

~CircularDynamicArray();

Destructor for the class.

O(1)

elmtype& operator[](int i);

Traditional [] operator. Should print a message if i is

O(1)

out of bounds and return a reference to value of type

elmtype stored in the class for this purpose..

void addEnd(elmtype v);

increases the size of the array by 1 and stores v at the

O(1)

end of the array. Should double the capacity when the

amortized

new element doesn’t fit.

void addFront(elmtype v);

increases the size of the array by 1 and stores v at the

O(1)

beginning of the array. Should double the capacity

amortized

when the new element doesn’t fit. The new element

should be the item returned at index 0.

void delEnd();

reduces the size of the array by 1 at the end. Should

O(1)

shrink the capacity when only 25% of the array is in use

amortized

after the delete.

void delFront();

reduces the size of the array by 1 at the beginning of

O(1)

the array. Should shrink the capacity when only 25% of

amortized

the array is in use after the delete.

int length();

returns the size of the array.

O(1)

int capacity();

returns the capacity of the array.

O(1)

int clear();

Frees any space currently used and starts over with an

O(1)

array of size 2.

Elmtype QuickSelect(int k);

returns the kth smallest element in the array using the

O(size)

quickselect algorithm.

expected

Elmtype WCSelect(int k);

returns the kth smallest element in the array using the

O(size)

worst case O(N) time algorithm.

void stableSort();

Sorts the values in the array using a comparison based

O(size lg size)

O(N lg N) algorithm. The sort must be stable.

void radixSort(int i);

Sorts the values in the array using a radix based sort on

O(i size)

the low order i bits of elmtype.

int linearSearch(elmtype e)

Performs a linear search of the array looking for the

O(size)

item e. Returns the index of the item if found or -1

otherwise.

int binSearch(elmtype e)

Performs a binary search of the array looking for the

O(lg size)

item e. Returns the index of the item if found or -1

otherwise. Assumes that the array is in sorted order.

Your class should include proper memory management, including a destructor, a copy constructor, and a copy assignment operator.
