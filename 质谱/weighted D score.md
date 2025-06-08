


> Written with [StackEdit中文版](https://stackedit.cn/).-   



**$\displaystyle \lambda$（lambda）**：**特异性因子**，衡量猎物蛋白 _j_ 出现的诱饵范围有多窄。定义为  
   $\ λj  =  k∑i=1kfi,j .\displaystyle \lambda_j \;=\; \frac{k}{\sum_{i=1}^{k} f_{i,j}}\,. λj​=∑i=1k​fi,j​k​.  
 分母$\sum_{i=1}^{k} f_{i,j}$表示猎物 _j_ 在多少个诱饵中被检出。如果 _j_ 只出现在1个诱饵中，那么分母=1，$\lambda = k$（取最大值，表明高度特异）；若 _j_ 普遍出现在所有 $k$ 个诱饵中，分母=$k$，则 $\lambda = 1$（最低特异性）【19†】。因此 $\lambda$ 值**越大**，说明猎物越“专一”于极少数诱饵，即可能是特定互作蛋白；$\lambda=1$ 则意味着猎物几乎是“到处都是”，很可能是背景蛋白。需要注意的是，为防止某些猎物出现在过多诱饵中导致 $\lambda<1$，通常$\lambda$下限设为1（即$\lambda_j$不会小于1）【19†】。
    
-   **$\displaystyle \bar{X}_j$**：猎物 _j_ 在所有诱饵中谱图计数的平均值，计算方式为 $\bar{X}_j = \frac{1}{k}\sum_{i=1}^k x_{i,j}$。这是针对猎物 _j_ 的**总体丰度水平**。
    
-   **$\displaystyle \sigma_j$**：猎物 _j_ 在不同诱饵间谱图计数的标准差，可用公式 $\sigma_j = \sqrt{\frac{1}{k}\sum_{i=1}^k (x_{i,j} - \bar{X}_j)^2}$ 计算。$\sigma_j$反映该猎物丰度分布的**离散程度**。
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTcwNzIzMjA3OF19
-->