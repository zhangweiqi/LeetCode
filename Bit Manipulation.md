## 461. Hamming Distance

 - url:https://leetcode.com/problems/hamming-distance/description/
 - analysis:
 - solution:

```python
class Solution(object):
    def hammingDistance(self, x, y):
        """
        :type x: int
        :type y: int
        :rtype: int
        """
        res = 0
        x = bin(x)[2:]
        y = bin(y)[2:]
        if len(x) == len(y):
            for i in xrange(len(x)):
                if x[i] != y[i]:
                    res += 1
            return res
        length = max(map(len, [x, y]))
        if len(x) < length:
            diff = length - len(x)
            str_0 = ''
            for i in xrange(diff):
                str_0 += '0'
            x = str_0 + x
            for i in xrange(len(y)):
                if x[i] != y[i]:
                    res += 1
            return res
        else:
            diff = length - len(y)
            str_0 = ''
            for i in xrange(diff):
                str_0 += '0'
            y = str_0 + y
            for i in xrange(len(x)):
                if x[i] != y[i]:
                    res += 1
            return res
```
---------
