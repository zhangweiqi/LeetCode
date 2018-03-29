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
 - analysis: 注意T中可以有重复的字母
 - solution:
 
 ```python
class Solution(object):
    def customSortString(self, S, T):
        """
        :type S: str
        :type T: str
        :rtype: str
        """
        T = list(T)
        for s in S:
            for i in range(T.count(s)):
                T.remove(s)
                T.append(s)
        res = ""        
        for t in T:        
           res += str(t) 
        return res
```

----------------
## 557.Reverse Words in a String III

 - url:
 - analysis:
 - solution:
 
```python
class Solution(object):
    def reverseWords(self, s):
        """
        :type s: str
        :rtype: str
        """
        s_list = s.split(" ")
        s_reverse = [i[::-1] for i in s_list]
        res = " ".join(s_reverse)
        return res
```
-------------
## 521.Longest Uncommon Subsequence I

 - url:
 - analysis: 关键要理解题意
 - solution:
 
 ```python
class Solution(object):
    def findLUSlength(self, a, b):
        """
        :type a: str
        :type b: str
        :rtype: int
        """
        return -1 if a == b else max(len(a), len(b))
```
-------------
## 553.Optimal Division

 - url:
 - analysis: 仔细分析问题，弄清数学方法后，分情况用代码搞定
 - solution:
 
 ```python
class Solution(object):
    def optimalDivision(self, nums):
        """
        :type nums: List[int]
        :rtype: str
        """
        if len(nums) == 1:
            return str(nums[0])
        if len(nums) == 2:
            return "/".join([str(num) for num in nums])
        else:
            return str(nums[0]) + '/(' + "/".join([str(num) for num in nums[1:]]) + ')'
```
--------------
## 647.Palindromic Substrings

 - url:
 - analysis:
 - solution:
 
```python
class Solution(object):
    def countSubstrings(self, s):
        """
        :type s: str
        :rtype: int
        """
        length = len(s)
        res = len(s)
        for i in range(2, length+1):
            for j in range(length-i+1):
                if s[j:j+i] == s[j:j+i][::-1]:
                    res += 1
        return res       
```
--------------
## 609.Find Duplicate File in System
 - url:
 - analysis:
 - solution:
 
 ```python

```
-------------
## 520.Detect Capital
 
 - url:
 - analysis:
 - solution:

```python
class Solution(object):
    def detectCapitalUse(self, word):
        """
        :type word: str
        :rtype: bool
        """
        if word.islower():
            return True
        elif word.istitle():
            return True
        elif word.isupper():
            return True
        else:
            return False
        
``` 

------------
## 788.Rotated Digits
 - url:https://leetcode.com/problems/rotated-digits/description/
 - analysis: 理清思路再写
 - solution:
 
 ```python
class Solution(object):
    def rotatedDigits(self, N):
        """
        :type N: int
        :rtype: int
        """
        res = 0
        for i in range(1, N+1):
            i_str = str(i)
            i_str_reverse = ""
            if '3' in i_str or '4' in i_str or '7' in i_str:
                continue
            for j in i_str:
                if j == '2':
                    i_str_reverse += '5'
                elif j == '5':
                    i_str_reverse += '2'
                elif j == '6':
                    i_str_reverse += '9'
                elif j == '9':
                    i_str_reverse += '6'
                else:
                    i_str_reverse += j    
            if i_str_reverse != i_str:
                res += 1        
        return res
```
-------------
## 696.Count Binary Substrings
  - url:https://leetcode.com/problems/count-binary-substrings/description/
  - analysis: 先将字符串格式化为另一种方便处理的格式，然后再处理
              注意使用了map zip
  - solution:
  
```python
class Solution(object):
    def countBinarySubstrings(self, s):
        """
        :type s: str
        :rtype: int
        """
        s = map(len, s.replace('01', '0 1').replace('10', '1 0').split())
        return sum(min(a, b) for a, b in zip(s, s[1:]))

```
------------
## 606.Construct String from Binary Tree
 - url:https://leetcode.com/problems/construct-string-from-binary-tree/description/
 - analysis:
 -solution:

```python

```

