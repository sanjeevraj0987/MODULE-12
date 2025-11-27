# Ex.No:1  
# Ex.Name: Deletion in Binary Search Tree (BST)  

## Date:  

## Aim:  
To write a C++ function to perform **deletion in a Binary Search Tree (BST)**.  
The deletion should handle the three standard cases:  
1. Node to be deleted has no child (leaf node).  
2. Node to be deleted has one child.  
3. Node to be deleted has two children (in this case, the inorder successor is needed, which is the minimum value node in the right subtree).  

## Algorithm:  
1. Start the program.  
2. Define a `Node` structure with `data`, `left`, and `right` pointers.  
3. Define a function `minValueNode(Node* root)` to find the minimum value node in the right subtree.  
4. Define a function `deleteNode(Node* root, int key)`:  
   - If the key is less than the root’s data → recur for the left subtree.  
   - If the key is greater than the root’s data → recur for the right subtree.  
   - If the key matches the root’s data:  
     - If the node has no child → return `NULL`.  
     - If the node has one child → return the non-null child.  
     - If the node has two children → replace the node with its inorder successor (minimum in right subtree) and delete the inorder successor.  
5. Perform inorder traversal before and after deletion to show results.  
6. Stop the program.  

## Program:
```cpp
BST* BST ::deleteNode(BST* root, int value)
{
    
 //write your code here
    if(value < root -> data)
        root -> left = deleteNode(root-> left, value);
 
    else if (value > root->data)
        root->right = deleteNode(root->right, value);
 
   
    else {
       if (root->left==NULL and root->right==NULL)
            return NULL;
       
        
        else if (root->left == NULL) {
            BST* temp = root->right;
            
            free(root);
            return temp;
        }
        else if (root->right == NULL) {
            BST* temp = root->left;
            free(root);
            return temp;
        }
 
       
       BST* temp = minValueNode(root->right);
 
        
        root->data = temp->data;
 
    
        root->right = deleteNode(root->right, temp->data);
    }
    return root;

}

```

## Output:
<img width="872" height="499" alt="image" src="https://github.com/user-attachments/assets/093a30fe-cd30-4541-8dbc-d96aaa422d6e" />

## Result:
The Program Executed Successfully.

