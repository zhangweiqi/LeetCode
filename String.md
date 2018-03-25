## 771.Jewels and Stones

 - url:
 - analysis:遍历
 - solution:
 
 ```python
class Solution(object):
    def numJewlsInStones(self, J, S):
        """
        :type J:str
        :type S:str
        :rtype: int
        """
        num = 0
        for i in set(J):
            num += S.count(i)
        return num
 ```

----------
## 344.Reverse String

 - url:
 - analysis: 1.切片  beat 7% 2.列表反转 beat 56%
 - solution:
 
 ```python
class Solution(object):
    def reverseString_chip(self, s):
        """
        :type s: str
        :rtypr: str
        """
        return s[::-1]
        
    def reverseString_list(self, s):
        """
        :type s: str
        :rtype: str
        """
        sList = list(s)
        sList = sList.reverse()
        sReverse = "".join(sList)
        return sReverse
```