## 338.Counting Bits

 - url:
 - analysis: 用现成轮子就是开心
 - solution:
 
 ```python
class Solution(object):
    def countBits(self, num):
        """
        :type num: int
        :rtype: List[int]
        """
        numlist = range(num+1)
        returnlist = []
        for i in numlist:
            count = 0
            i = str(bin(i))
            returnlist.append(i.count('1'))
        return returnlist
```



----------



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
## 283.Move Zeroes

 - url:
 - analysis: 1.遍历，然后分为两个队列相加  80ms  2.遍历，然后移出0并append 0  299ms
 - soulution:
 ```python
class Solution(object):
    def moveZeroes_1(self, nums):
        """
        :type nums: List[int]
        :rtype: None
        """
        # 为何要加[:]?
        nums[:] = [i for i in nums if i] + [i for i in nums if not i]
        
    def moveZeroes_2(self, nums):
        # nums在for循环定义中确定，在循环中改变该变量不影响循环
        for num in nums:
            if num == 0:
                nums.remove(0)
                nums.append(0)
```

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
