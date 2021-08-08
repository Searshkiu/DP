# DP
Notes made when studying dynamic programming  
### 01. 背包问题
强烈推荐 [背包九讲](https://www.kancloud.cn/kancloud/pack/70124)
#### 基本思想
限制：背包容量w，每件物品有重量w与价值v  
问题特点：对于每件物品有有限种状态，通过枚举每件物品的状态，以最值推最值
#### 01背包
#### 完全背包
### 02. 区间DP
#### 状态转移方程
求累计价值的最大值时：用f[i][j]表示在区间[i,j]中可以取到的最大值，k∈[i,j]表示枚举的合并点，则  
***f[i][j]=max( f[i][j], f[i][k]+f[k+1][j]+cost )***  
  
注意检查转移前后的状态是否**有意义**，如LGR [P3146 [USACO16OPEN]248 G](https://www.luogu.com.cn/problem/P3146) 这道题里面，如果分段的两部分函数值相等，有两种情况：一种是确实合并完得到的函数值相等，一种是没有合并过，二者的函数值都为0.
### 涉及题单  
背包问题：洛谷 [背包问题（简单）](https://www.luogu.com.cn/training/8917)  
区间DP：洛谷 [可达部落 区间动态规划](https://www.luogu.com.cn/training/55511#problems)  
Mark: www.oi-wiki.org
