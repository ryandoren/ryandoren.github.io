---
title: LeetCode with Python
author: "Ryan"              # 文章作者
description : "Tearing LeetCode Problems"    # 文章描述信息
date: 2021-1-5            # 文章编写日期
draft: false
---
# 2020名企高频面试题
## 经典题目
### [53. 最大子序和](https://leetcode-cn.com/problems/maximum-subarray/solution/zui-da-zi-xu-he-by-leetcode-solution/)
> 知识点：数组；前缀和；哨兵；动态规划；贪心；分治
- 题目描述：

给你一个整数数组 nums ，请你找出一个具有最大和的连续子数组（子数组最少包含一个元素），返回其最大和。

示例 1：
```
输入：nums = [-2,1,-3,4,-1,2,1,-5,4]
输出：6
解释：连续子数组 [4,-1,2,1] 的和最大，为 6 。
```
示例 2：
```
输入：nums = [1]
输出：1
```
示例 3：
```
输入：nums = [5,4,-1,7,8]
输出：23
```

- 提示：

1 <= nums.length <= 105
104 <= nums[i] <= 104

- 进阶：如果你已经实现复杂度为 O(n) 的解法，尝试使用更为精妙的 分治法 求解。

法一：动态规划，复杂度`!$O(n)$`
```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        pre, maxValue = 0, nums[0]
        for i in range(len(nums)):
            pre = max(pre+nums[i], nums[i])
            maxValue = max(maxValue, pre)
        return maxValue
```

### 合并两个有序数组

### 买卖股票的最佳时机

### 验证回文串

### 二叉树的层序遍历

### 复制带随机指针的链表

### LRU缓存机制

### 岛屿数量

### 接雨水

### 最小覆盖子串

## 主题要点
无论你是面试什么岗位，面试官基本都会从以下几个方面全面考察候选人的技术水平。当然，除了这些面试考点以外，你还需要了解目标岗位的其他技术要求，及时查漏补缺，充分备战技术面试。
![enter description here](./images/1641198493190.png)
算法和数据结构一直是技术面试的重点和难点。近年来，很多知名企业如谷歌, 脸书等在面试过程中都会有特定的电话面试环节, 专门用来面算法题。这些企业通常会使用在线协同代码编程网站，需要面试者用一小时解决 4 道算法问题，面试官可以实时看到候选人所写的代码。除了远程面试外, 在 Onsite 面试中还会有白板写代码等环节。
 ![enter description here](./images/1641198518115.png)
 
## 名企面试重点梳理
与其他公司相比，头部互联网公司对面试者的算法水平要求更高，经常出中等及以上难度的题目。不止要求面试者能写出算法，还要求时间复杂度最小，找出最优方式，这就需要我们针对一道题目思考多种解决办法；同时需要注意算法中对异常情况的处理。
![enter description here](./images/1641198607924.png)
除了这些算法外，有的面试官还会临时给一些有规律的数据，让你写出一种算法或给出思路，考验你的逻辑思维能力。想要锻炼算法思维，在学习过程中，需要先掌握一类算法，钻研透了再去掌握另一类，这样在遇到新问题时才能举一反三。在面试中如果遇到卡壳的情况也不用太紧张，面试官会给你一定的提示，你可以根据已掌握的算法，尽量说出解题思路，在思考的过程中也能消除紧张，也许很快就能想出问题的解答思路。

## 数组
### 寻找两个正序数组的中位数

### 盛最多水的容器

### 三数之和

### 下一个排列

### 搜索旋转排序数组

### 在排序数组中查找元素的第一个和最后一个位置

### 螺旋矩阵

### 合并区间

### 除自身以外数组的乘积

### 最后一块石头的重量 Ⅱ

## 字符串
### 整数转换英文表示

### 字符串相加

### 验证回文字符串 Ⅱ

### 最常见的单词

### 重新排列日志文件

## 链表
### 两数相加

### 无重复字符串的最长子串

### 删除链表的倒数第N个节点

### 合并两个有序链表

### 反转链表


# 算法面试题汇总
## 开始之前
### 136. [只出现一次的数字](https://leetcode-cn.com/problems/single-number/solution/zhi-chu-xian-yi-ci-de-shu-zi-by-leetcode-solution/)
> 知识点：异或、位运算、集合
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
> 🐍规律总结：
> a ^ a = 0；自异或结果为0
> a ^ 0 = a；与0异或结果为自身
> a ^ b ^ c = a ^ c ^ b；异或运算具有交换律

