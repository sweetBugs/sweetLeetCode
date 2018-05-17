# sweetLeetCode
## 1. Two Sum
> 给定一个list，和一个target，要求在list中找到两个元素，使其和为该target，输出这两个元素的index。例如Given nums = [2, 7, 11, 15], target = 9, Because nums[0] + nums[1] = 2 + 7 = 9, return [0, 1].

### Code
    class Solution:
        def twoSum(self, nums, target):
            """
            :type nums: List[int]
            :type target: int
            :rtype: List[int]
            """
            p = list(range(1000))
            n = []
            for i in p:
                n.append(-i)
            l = p + n
            l.remove(0)
            for i in l:
                if i in nums:
                    num1 = nums.index(i)
                    nums[num1]= 'ok'
                    left = target - i
                    if left in nums:
                        num2 = nums.index(left)
                        break
            if i == 1000:
                print("no answer")
            return [num1, num2]
### Remark
- **很困难很困难很困难!** 重要的事说三遍！python还没学完就来刷题可能是一个错误，easy类别里面的第一道题，思路不难，可是自己很难实现，前前后后subscribe了五六次才成功，代码运行速度也比别人的慢很多，渣硕还有很长的路要走。**不过真的给leetcode点赞，好喜欢！**（当然也要给github点赞：））
- **遇到的几个问题：** 1. 没考虑list中会出现相同的两个数；2. 没考虑负数。
- **后天非参数统计考试加油！！！** 
***


## 7. Two Sum
> Given a 32-bit signed integer, reverse digits of an integer.例如input：123，output：321；input：-123，output：-321；input：120，output：21.

### Code
    class Solution:
    def reverse(self, x):
        """
        :type x: int
        :rtype: int
        """
        y = str(abs(x))
        n = len(y)
        t = 0      
        for i in range(n):
            t += int(y[i])*10**(i)
        if abs(t) < 2**31:
            if x < 0:
                return -t
            else:
                return t
        else:
            return 0
***


## 9. Palindrome Number
> Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.例如121是回文而-121就不是，101是回文而10不是.
### Code
    class Solution:
    def isPalindrome(self, x):
        """
        :type x: int
        :rtype: bool
        """
        y = 0
        z = x
        if x >= 0:
            while x >= 10:
                t = x%10
                y = y*10 + t
                x = (x - t)/10
            y = y*10 + x
            return y == z
        else:
            return False
