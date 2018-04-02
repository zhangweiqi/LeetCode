## 807. Max Increase to Keep City Skyline

 - url:https://leetcode.com/problems/max-increase-to-keep-city-skyline/description/
 - analysis:
 - solution:

```python

```
-----------------
## 804. Unique Morse Code Words

 - url:https://leetcode.com/problems/unique-morse-code-words/description/
 - analysis:
 - solution:

```python

```
-----------
## 797. All Paths From Source to Target

 - url:
 - analysis:
 - solution:


```python

```
----------
## 806. Number of Lines To Write String

 - url:https://leetcode.com/problems/number-of-lines-to-write-string/description/
 - analysis:
 - solution:

```python
class Solution(object):
    def numberOfLines(self, widths, S):
        """
        :type widths: List[int]
        :type S: str
        :rtype: List[int]
        """
        res, cur = 1, 0
        for i in S:
            width = widths[ord(i) - ord('a')]
            res += 1 if cur + width > 100 else 0
            cur = width if cur + width > 100 else cur + width
        return [res, cur]
```
------
##
