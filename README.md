# array-16bits


In the context of the given information, it appears that an array is a sequence of values stored in memory, with the array definition specifying the number of bits per value and the number of values in the array. The array definition also returns a pointer to the start of the array in memory and the length of the array in terms of the number of values or bytes.

For example, an array defined as "array 16bits [1 2 3 4]" would create an array of 4 16-bit values, and the definition would return a pointer to the start of the array and the length of the array in words (i.e., 4). To access a value in the array, the pointer is used to locate the start of the array in memory, and an offset is added to the pointer to move to the desired value in the array. For example, to access the 3rd value in the array, we would calculate the offset as 3 * 2 (since each value in the array occupies 2 bytes) and add this to the pointer to find the address of the 3rd value. Then, the value at this address can be fetched.

Similarly, an array defined as "array byte 8 bits [10 20 30 40 50]" would create an array of 5 8-bit values, and the definition would return a pointer to the start of the array and the length of the array in bytes (i.e., 5). To access a value in this array, we would use the pointer to locate the start of the array in memory, and add the index of the desired value to the pointer to find the address of the value. For example, to access the 2nd value in the array, we would add 2 to the pointer to find the address of the 2nd value, and then fetch the value at this address.

## examples using arrays with 16-bit elements:

Defining and printing an array of 16-bit integers:
```
[ 100 200 400 800 ] .s
```
This code defines an array with 4 elements and prints its address and length on the stack. The array is stored in the heap.

Storing the pointer to an array in a variable and accessing an element:
```
[ 100 200 400 800 ] ' c!
c@ 3 2 * + @ .
```
This code stores the pointer to the array in the variable c and then retrieves the third element of the array (which is 400).

Modifying an element of an array:
```
[ 100 200 400 800 ] ' c!
c@ 3 2 * + !
```
This code stores the value 500 in the third element of the array (which was previously 400).

## Here are some examples using arrays with 8-bit elements:

Defining and printing a byte array:
```
\[ 10 20 30 40 50 ] .s
```
This code defines a byte array with 5 elements and prints its address and length on the stack. The array is stored in the heap.

Storing the pointer to a byte array in a variable and accessing an element:
```
\[ 10 20 30 40 50 ] ' b!
b@ 2 + \@ .
```
This code stores the pointer to the byte array in the variable b and then retrieves the second element of the array (which is 20).

Modifying an element of a byte array:
```
\[ 10 20 30 40 50 ] ' b!
b@ 2 + \!
```
This code stores the value 25 in the second element of the byte array (which was previously 20).


## see sorting
- https://github.com/SteveJustin1963/sort


