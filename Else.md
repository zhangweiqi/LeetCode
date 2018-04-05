## 807. Max Increase to Keep City Skyline

 - url:https://leetcode.com/problems/max-increase-to-keep-city-skyline/description/
 - analysis:
 - solution:

```python
class Solution(object):
    def maxIncreaseKeepingSkyline(self, grid):
        """
        :type grid: List[List[int]]
        :rtype: int
        """
        res = 0
        length = len(grid)
        wide = len(grid[0])
        
        for i in xrange(length):
            for j in xrange(wide):
                i_max = max(grid[i])
                j_max = max([grid[item][j] for item in xrange(length)])
                res += min(i_max, j_max) - grid[i][j]
        return res        
```
-----------------
## 804. Unique Morse Code Words

 - url:https://leetcode.com/problems/unique-morse-code-words/description/
 - analysis:
 - solution:

```python
class Solution(object):
    def uniqueMorseRepresentations(self, words):
        """
        :type words: List[str]
        :rtype: int
        """
        d = [".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ".---", "-.-", ".-..", "--",
             "-.", "---", ".--.", "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--.."]
        res = []
        for word in words:
            morse = ""
            for s in word:
                morse += d[ord(s) - ord("a")]
            res.append(morse)
        return len(set(res))
```
-----------
## 797. All Paths From Source to Target

 - url:https://leetcode.com/problems/all-paths-from-source-to-target/description/
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
        # res为占用的行数，cur为最后一行的占用单元数
        # 初始化res，cur
        res, cur = 1, 0
        for i in S:
            # 得到单个字符串的占用长度
            width = widths[ord(i) - ord('a')]
            res += 1 if cur + width > 100 else 0
            cur = width if cur + width > 100 else cur + width
        return [res, cur]
```
------
##
