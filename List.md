## 136.Single Number
 
 - url:
 - analysis: 利用异或（XOR）运算
             A XOR A = 0, 且异或运算可交换， 故
             （2^1^4^5^2^4^1）= ((2^2)^(4^4)^(1^1)^5) = (0^0^0^5) = 5
 - solution:
 
 ```python
class Solution(object):
    def singleNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        res = 0
        for num in nums:
            res = res^num
        return res
        
```



----------
## 260.Single Number III

 - url:
 - analysis:
 - solution:
 ```python
class Solution(object):
    def singleNumber(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        unique = set()
        double = set()
        for i in nums:
            if i not in unique:
                unique.add(i)
            else:
                double.add(i)
        return list(unique-double)
```
-------------
## 134.Intersection of Two Arrays

 - url:
 - analysis: 
 - soulution:
 
```python
class Solution(object):
    def intersection(self, nums1, nums2):
        """
        :type nums1: List[int]
        :type nums2: List[int]
        :rtype: List[int]
        """
        return list(set(nums1)&set(nums2))
```
