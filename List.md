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
