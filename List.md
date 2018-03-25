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