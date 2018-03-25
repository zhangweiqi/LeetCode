## 654.Maximum Binary Tree

 - url:
 - analysis:显然用递归
 - solution:
 
 ```python
# Definition for a binary tree node.
class TreeNode(object):
   def __init__(self, x):
       self.val = x
       self.left = None
       self.right = None
       
       
class Solution(object):
    def constructMaximumBinaryTree(self, nums):
        """
        :type nums: List[int]
        :rtype: TreeNode
        """
        if nums:
            # max的位置
            point = nums.index(max(nums))
            # 定义根节点
            root = TreeNode(nums[point])
            # 左结点
            root.left = self.constructMaximumBinaryTree(nums[:point])
            # 右结点
            root.right = self.constructMaximumBinaryTree(nums[point+1:])
            return root
```