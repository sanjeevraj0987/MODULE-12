# Ex.No:5  
# Ex.Name: Merge Sort – merge Module  

## Date:  

## Aim:  
To write a C++ program to implement **Merge Sort** and include a module to **merge subarrays** and print the array before and after sorting.  

## Algorithm:  
1. Start the program.  
2. Input the size `n` and elements of the array.  
3. Define a function `merge(arr, l, m, r)` that:  
   - Creates two temporary subarrays.  
   - Merges them back into the original array in sorted order.  
4. Define a recursive function `mergeSort(arr, l, r)` that:  
   - Divides the array into two halves.  
   - Calls itself for each half.  
   - Calls `merge()` to combine them.  
5. Define a function `printArray(arr, n)` to print the elements.  
6. In `main()`:  
   - Print the array before sorting.  
   - Call `mergeSort()`.  
   - Print the array after sorting.  
7. Stop the program.  

## Program:
```cpp
void merge(int arr[], int l, int m, int r)
{
    int i,j,k;
    int n1=m-l+1;
    int n2=r-m;
    
    int L[n1],R[n2];
    for(i=0; i<n1; i++)
        L[i]=arr[l+i];
    for(j=0; j<n2; j++)
        R[j]=arr[m+1+j];
    
    i=0;
    j=0;
    k=l;
    while(i<n1 && j<n2)
    {
        if(L[i]<=R[j])
        {
            arr[k]=L[i];
            i++;
        }
        else
        {
            arr[k]=R[j];
            j++;
        }
        k++;
    }
    while(i<n1)
    {
        arr[k]=L[i];
        i++;
        k++;
    }
    while(j<n2)
    {
        arr[k]=R[j];
        j++;
        k++;
    }
}
```

## Output:
<img width="873" height="454" alt="image" src="https://github.com/user-attachments/assets/70fd1c12-b20b-46e3-8e73-b433f30666c3" />

## Result:
The Program Executed Successfully.
