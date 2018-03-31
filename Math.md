## 292.Nim Game

 - url:
 - analysis: 弟弟用小学奥数解决了...
             问题关键是两个人一次加起来取4个
 - solution:
 
 ```python
 class Solution(object):
    def canWinNim(self, n):
        """
        :type n:int
        :rtype: bool
        """
        return bool(n%4)

```
## 258.Add Digits

 - url:
 - analysis:
 - solution:
 
 ```python
class Soulution(object):
    def addDigits(self, num):
        """
        :type num: int
        :rtype: int
        """
        while num >= 10:
            result = 0
            while num != 0:
                result = result + num%10
                num = num/10
            num = result
        return num
```

------------
