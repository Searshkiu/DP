# DP
Notes made when studying dynamic programming  

---

### 01. 背包问题
强烈推荐 [背包九讲](https://www.kancloud.cn/kancloud/pack/70124)
#### 基本思想
限制：背包容量w，每件物品有重量w与价值v  
问题特点：对于每件物品有有限种状态，通过枚举每件物品的状态，以最值推最值
#### 01背包
#### 完全背包
---
### 02. 区间DP
#### 状态转移方程
求累计价值的最大值时：用f[i][j]表示在区间[i,j]中可以取到的最大值，k∈[i,j]表示枚举的合并点，则  
***f[i][j]=max( f[i][j], f[i][k]+f[k+1][j]+cost )***  
#### 常见问题类型  
绝对会出现的游戏中的操作：
**合并**  
很多解释可以理解为合并，例如折叠。只要是一条串里面的某些元素~~不明不白地~~可以（按照一定规则）消失，那么就可以解释为**合并**。  
例如最经典的石子合并和[P4302 [SCOI2003]字符串折叠](https://www.luogu.com.cn/problem/P4302)（折叠是有特殊条件的合并，这道题也跟回文有关）  
**或分离**  

对于串：  
两头进行加删操作 计数最值题 例如[P3205 [HNOI2010]合唱队](https://www.luogu.com.cn/problem/P3205)和[P1005 [NOIP2007 提高组] 矩阵取数游戏](https://www.luogu.com.cn/problem/P1005)  
or 与回文有关的操作最值 例如[P4170 [CQOI2007]涂色](https://www.luogu.com.cn/problem/P4170)
  
#### 注意
- 检查转移前后的状态是否**有意义**，如LGR [P3146 [USACO16OPEN]248 G](https://www.luogu.com.cn/problem/P3146) 这道题里面，如果分段的两部分函数值相等，有两种情况：一种是确实合并完得到的函数值相等，一种是没有合并过，二者的函数值都为0.  
- 还有一点：注意思维的灵活性，该增加维度就增加维度。例如[P3205 [HNOI2010]合唱队](https://www.luogu.com.cn/problem/P3205)，增加了一维表示当前考虑到区间里最最左边或最右边的数的上一个数是从最左边进入的还是从右边进入的（因为当前加数策略与上一步加数策略是什么有关）和[P1043 [NOIP2003 普及组] 数字游戏](https://www.luogu.com.cn/problem/P1043)（直接加了一维表示分割的区间数~~为啥捏~~）

---

### 涉及题单  
背包问题：洛谷 [背包问题（简单）](https://www.luogu.com.cn/training/8917)  
区间DP：洛谷 [可达部落 区间动态规划](https://www.luogu.com.cn/training/55511#problems)  
Mark: www.oi-wiki.org
