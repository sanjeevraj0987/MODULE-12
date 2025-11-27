# Ex.No:4  
# Ex.Name: Quick Sort – printArray Module  

## Date:  

## Aim:  
To write a C++ program to implement **Quick Sort** and include a module to **print the array before and after sorting**.  

## Algorithm:  
1. Start the program.  
2. Input the size `n` and elements of the array.  
3. Define a function `partition(arr, low, high)` that:  
   - Selects the pivot element.  
   - Places all smaller elements to the left of the pivot and larger elements to the right.  
   - Returns the pivot index.  
4. Define a recursive function `quickSort(arr, low, high)` that:  
   - Calls `partition()`.  
   - Recursively sorts the left and right subarrays.  
5. Define a function `printArray(arr, n)` to print the array elements.  
6. In `main()`:  
   - Print the array before sorting.  
   - Call `quickSort()`.  
   - Print the array after sorting.  
7. Stop the program.  

## Program:
```cpp
void printArray(int array[], int size){
    for(int i=0;i<size;i++){
        cout<<array[i]<<" ";
    }
    cout<<endl;
}
```

## Output:
<img width="868" height="467" alt="image" src="https://github.com/user-attachments/assets/706050d0-dbbb-46b8-b2e9-781db13ca168" />

## Result:
The Program Executed Successfully.


