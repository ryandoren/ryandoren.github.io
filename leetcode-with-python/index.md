# LeetCode with Python

# Microsoft
## 经典题目
### 最大子序和

# 算法面试题汇总
## 开始之前
### 只出现一次的数字
- 题目描述：

给定一个非空整数数组，除了某个元素只出现一次以外，其余每个元素均出现两次。找出那个只出现了一次的元素。 

示例 1: 
```
输入: [2,2,1] 
输出: 1 
```
示例 2: 
```
输入: [4,1,2,1,2] 
输出: 4 
```
- 说明： 

你的算法应该具有线性时间复杂度。 你可以不使用额外空间来实现吗？ 

- 提示：位运算、集合
- 代码：
```python
class Solution:
    def singleNumber(self, nums: List[int]) -> int:
        target=0
        for i in range(len(nums)):
            target=target^nums[i]
        return target
```
> 🐍Python 异或（exclusive or，^）：**A B有且仅有一者为真**
> 🐍计算过程：基于二进制基础上，将A ^ B **按位**异或的过程为，先将A和B分别转换为二进制，按位异或得到结果后再组合起来，最后转换为十进制。
> ![enter description here](./images/1641194916400.png)
> 🐍例如：5 ^ 3 的结果为6是因为
> 5 = 0101(b)
> 3 = 0011(b)
> 0^0 ->0
> 1^0 ->1
> 0^1 ->1
> 1^1 ->0
> 0110(b) 转换为十进制：6



