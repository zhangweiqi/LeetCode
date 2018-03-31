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
## 535. Encode and Decode TinyURL

 - url:https://leetcode.com/problems/encode-and-decode-tinyurl/description/
 - analysis:
 - solution:

```python

```