# Ex.No:3  
# Ex.Name: Binary Search Module  

## Date:  

## Aim:  
To write a C++ program to implement the **Binary Search Algorithm** to find whether an element is present in a sorted array and return its position.  

## Algorithm:  
1. Start the program.  
2. Input the number of elements `n` and the array elements (sorted in ascending order).  
3. Input the element `key` to be searched.  
4. Initialize two variables:  
   - `low = 0` (first index)  
   - `high = n-1` (last index).  
5. Repeat while `low <= high`:  
   - Find `mid = (low + high) / 2`.  
   - If `arr[mid] == key`, return the position.  
   - If `arr[mid] > key`, set `high = mid - 1`.  
   - If `arr[mid] < key`, set `low = mid + 1`.  
6. If the element is not found, print **"Element Not Found"**.  
7. Stop the program.  

## Program:
```cpp
int BS(int a[], int n, int search)
{
    int beg=0, end=n, mid;
    
    while(beg <= end)
    {
        mid = (beg+end)/2;
        if(a[mid]==search)
        {
            cout<<"Element found at "<<mid+1<<" position";
            return 1;
            break;
        }
        else if(a[mid] > search)
            end = mid-1;
        else
            beg = mid+1;
    }
    return 0;
}
```

## Output:
<img width="863" height="533" alt="image" src="https://github.com/user-attachments/assets/d1e0d6a4-bdb5-42bf-9de3-5f4b3b3e9327" />

## Result:
The Program Executed Successfully.

