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
