## 283.Move Zeroes

 - url:
 - analysis: 1.遍历，然后分为两个队列相加  80ms  2.遍历，然后移出0并append 0  299ms
 - solution:
 ```python
class Solution(object):
    def moveZeroes_1(self, nums):
        """
        :type nums: List[int]
        :rtype: None
        """
        # 为何要加[:]?
        nums[:] = [i for i in nums if i] + [i for i in nums if not i]

    def moveZeroes_2(self, nums):
        # nums在for循环定义中确定，在循环中改变该变量不影响循环
        for num in nums:
            if num == 0:
                nums.remove(0)
                nums.append(0)
```
-------------
## 561.Array Partition I

 - url:
 - analysis: 关键要理解题意，找到解法
 - solution: beat 90%

```python
class Solution(object):
    def arrayPairSum(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        nums.sort()
        return sum(nums[::2])
```

------------
## 766.Toeplitz Matrix

 - url:
 - analysis:
 - solution:

```python
class Solution(object):
    def isToeplitzMatrix(self, matrix):
        """
        :type matrix: List[List[int]]
        :rtype: bool
        """
        length = len(matrix)
        wide = len(matrix[0])

        for row in xrange(length):
            for line in xrange(wide):
                tmp_row = row
                tmp_line = line
                tmp = []
                while tmp_row < length and tmp_line < wide:
                    tmp.append(matrix[tmp_row][tmp_line])
                    tmp_row += 1
                    tmp_line += 1
                if len(set(tmp)) != 1:
                    return False
        return True
```
------------
## 566. Reshape the Matrix

 - url:
 - analysis:
 - solution:

```python
class Solution(object):
    def matrixReshape(self, nums, r, c):
        """
        :type nums: List[List[int]]
        :type r: int
        :type c: int
        :rtype: List[List[int]]
        """
        if len(nums)*len(nums[0]) != r*c:
            return nums
        else:
            tmp = []
            for i in nums:
                for j in i:
                    tmp.append(j)
            res = []
            for i in xrange(r):
                res.append([])
                for j in xrange(c):
                    res[i].append(tmp.pop(0))
        return res
```

----------------
## 442. Find All Duplicates in an Array

 - url:
 - analysis:
 - solution:

```python
class Solution(object):
    def findDuplicates(self, nums):
        """
        :type nums: List[int]
        :rtype: List[int]
        """
        res = []
        nums.sort()
        for i in xrange(len(nums)-1):
               if  nums[i] == nums[i+1]:
                    res.append(nums[i])
        return res
```
---------------
## 485. Max Consecutive Ones

 - url:
 - analysis:
 - solution:

```python
class Solution(object):
    def findMaxConsecutiveOnes(self, nums):
        """
        :type nums: List[int]
        :rtype: int
        """
        tmp = ''
        for num in nums:
            tmp += str(num)
        tmp = tmp.replace('10', '1 0').replace('01', '0 1')
        tmp = tmp.split(' ')
        tmp = [i for i in tmp if int(i) != 0]
        tmp = map(len, tmp)
        if tmp == []:
            return 0
        else:
            return max(tmp)
```
------------
## 