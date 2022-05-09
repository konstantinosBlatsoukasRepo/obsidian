                                    
             1                      
            / \                     
           /   \                    
        2 -     -3                  
        / \                         
       /   \                        
      /     \                       
   4 -       - 5

Depth First Traversals:   
(a) Inorder (Left, Root, Right) : 4 2 5 1 3   
(b) Preorder (Root, Left, Right) : 1 2 4 5 3   
(c) Postorder (Left, Right, Root) : 4 5 2 3 1  
Breadth-First or Level Order Traversal: 1 2 3 4 5




```python

# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution(object):
    def preorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        return self.travserse(root, [])
        
    def travserse(self, root, acc):
        if root is None:
            return acc
        
        if root.val is not None:
            acc.append(root.val)
            
        if root.left is not None:
            self.travserse(root.left, acc)
            
        if root.right is not None:
            self.travserse(root.right, acc)
            
        return acc
        
```


```python
# iterative solution using stack

# Definition for a binary tree node.

# class TreeNode(object):

#     def __init__(self, val=0, left=None, right=None):

#         self.val = val

#         self.left = left

#         self.right = right

class Solution(object):

    def preorderTraversal(self, root):

        """

        :type root: TreeNode

        :rtype: List[int]

        """

        result = []

        if root is None:
            return result

        stack = [root]

        while stack:            
            node = stack.pop() # remove last element from the top of the queue
            result.append(node.val)

            if node.right is not None:
                stack.append(node.right)

            if node.left is not None:
                stack.append(node.left)

  
        return result

```



```python 

#Post order traversal
# Definition for a binary tree node.
# class TreeNode(object):
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right
class Solution(object):
    def postorderTraversal(self, root):
        """
        :type root: TreeNode
        :rtype: List[int]
        """
        return self.travserse(root, [])
        
    def travserse(self, root, acc):
        if root is None:
            return acc

        if root.left is not None:
            self.travserse(root.left, acc)

        if root.right is not None:
            self.travserse(root.right, acc)
            
        if root.val is not None:
            acc.append(root.val)
    
        return acc

```