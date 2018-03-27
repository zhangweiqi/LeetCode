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
        sList.reverse()
        sReverse = "".join(sList)
        return sReverse
```
--------------
## 657.Judge Route Circle

 - url:
 - analysis: 
 - solution:
 ```python
class Solution(object):
    def judgeCircle(self, moves):
        """
        :type moves: str
        :rtype: bool
        """
        R = moves.count("R")
        L = moves.count("L")
        U = moves.count("U")
        D = moves.count("D")
        if R == L and U == D:
            return True 
        else:
            return False
```

-------------
## 537.Complex Number Multiplication
 - url:
 - analysis: 
 - solution:
 ```python
class Solution(object):
    def complexNumberMultiply(self, a, b):
        """
        :type a: str
        :type b: str
        :rtype: str
        """ 
        a1, a2 = map(int, a[:-1].split('+'))
        b1, b2 = map(int, b[:-1].split('+'))
        return '%d+%di' %(a1*b1-a2*b2, a1*b2+a2*b1)
 ```

------------
## 791.Custom Sort String
 - url:
 - analysis: 
 - solution:
 ```python

```
