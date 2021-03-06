# DP
Notes made when studying dynamic programming  

---

### 01. 背包DP
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
常见的游戏中的操作：  
**合并或分离**  
很多解释可以理解为合并，例如折叠。只要是一条串里面的某些元素~~不明不白地~~可以（按照一定规则）消失，那么就可以解释为**合并**。  
例如最经典的石子合并和[P4302 [SCOI2003]字符串折叠](https://www.luogu.com.cn/problem/P4302)（折叠是有特殊条件的合并，这道题也跟回文有关）  
**序列上的最短路径**  
[P1220 关路灯](https://www.luogu.com.cn/problem/P1220)  
[[IOI2000]邮局](https://www.luogu.com.cn/problem/P4767)

对于串：  
两头进行加删操作 计数最值题 例如[P3205 [HNOI2010]合唱队](https://www.luogu.com.cn/problem/P3205)和[P1005 [NOIP2007 提高组] 矩阵取数游戏](https://www.luogu.com.cn/problem/P1005)  
or 与回文有关的操作最值 例如[P4170 [CQOI2007]涂色](https://www.luogu.com.cn/problem/P4170)
  
#### 不知道啥
[[IOI2000]邮局](https://www.luogu.com.cn/problem/P4767)区间可以是前i个村庄，不一定要是从编号为i的村庄到编号为j的村庄。后者太乱了。采用前一种方法定义区间还可以省下一维。  
为什么可以这样做？  

#### 注意
- 检查转移前后的状态是否**有意义**，如LGR [P3146 [USACO16OPEN]248 G](https://www.luogu.com.cn/problem/P3146) 这道题里面，如果分段的两部分函数值相等，有两种情况：一种是确实合并完得到的函数值相等，一种是没有合并过，二者的函数值都为0.  
- 还有一点：注意思维的灵活性，该增加**维度**就增加维度。例如[P3205 [HNOI2010]合唱队](https://www.luogu.com.cn/problem/P3205)，增加了一维表示当前考虑到区间里最最左边或最右边的数的上一个数是从最左边进入的还是从右边进入的（因为当前加数策略与上一步加数策略是什么有关）和[P1043 [NOIP2003 普及组] 数字游戏](https://www.luogu.com.cn/problem/P1043)（直接加了一维表示分割的区间数~~为啥捏~~）. 至于为什么增加维度，还是要看纸笔推的状态转移方程. ~~如果发现写状态转移方程的时候要加文字说明，就加一维来表示文字辣QAQ~~

---
### 03.树上DP
---
### 04.状态压缩DP
---
### DP优化
#### 矩阵加速
矩阵乘法示意图：![矩](https://img2018.cnblogs.com/blog/1749451/201908/1749451-20190826113709947-2107024256.png "矩阵乘法示意图")

---
### 涉及题单  
背包问题：洛谷 [背包问题（简单）](https://www.luogu.com.cn/training/8917)  
区间DP：洛谷 [可达部落 区间动态规划](https://www.luogu.com.cn/training/55511#problems)  
Mark: www.oi-wiki.org
