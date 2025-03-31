> Written with [StackEdit中文版](https://stackedit.cn/).


# request 1
Although we have recently been able to solubilize CerS5 in a partially active form, we were unable to obtain enough material to determine the three-dimensional structure by cryo-electron microscopy at a high enough resolution. Thus, we persued a computational approach by comparing the predicted structures of CerS5 using RaptorX, trRosetta, RoseTTAfold, and AlphaFold2,. All four programs predicted a structure with a bundle of seven alpha-helices of ~30–50 Å length, with the N-terminus on one side of the membrane and the C-terminus and the Hox-like domain on the other side (Fig. 1B), consistent with earlier predictions. The AlphaFold2 structures of the six human CerS enzymes are very similar (Fig. 1C and Supplementary Table 1), which is expected in light of their high sequence similarity (Supplementary Table 2). 
请问什么是RMSD Value？

<img src="/imgs/2025-03-31/jwT1i7GxIdm9Rv5l.png" width="600" alt="Supplementary Table 1"/>


# reply 1
RMSD（Root-Mean-Square Deviation，均方根偏差）是结构生物学中用来衡量两个蛋白质三维结构之间差异的一个数值指标，单位是 Å（埃，1 Å = 0.1 纳米）。

简单来说，**RMSD 是衡量两个蛋白质结构是否相似的一个数字**：

-   如果 RMSD 值很小（比如 < 1 Å），说明两个结构几乎一样；
    
-   如果 RMSD 值较大（比如 > 2 Å），说明它们在三维空间中存在较大差异。

 
### 在你给的图中：

这个表格展示了 AlphaFold2 预测的 6 个 CerS 蛋白之间结构的 RMSD 值。

-   **对角线上方（白格子）是全长蛋白之间的 RMSD**。
    
-   **对角线下方（灰格子）是 TMD（跨膜结构域）之间的 RMSD**。
    
-   比如，CerS5 和 CerS6 的全长 RMSD 是 1.64 Å，而它们的 TMD RMSD 是 0.30 Å，说明它们的跨膜结构非常相似。
    

这正好呼应了你给的那段话：尽管 CerS5 活性不高、结构不能用 cryo-EM 解出来，但用 AlphaFold2 的预测结果来看，它的结构和其它 CerS 很相似，特别是在跨膜结构上（这是功能的关键部分之一）。

如果你想，我可以帮你可视化一下这张 RMSD 表的相似度趋势图，也可以讲讲 RMSD 是怎么算出来的。你想深入了解哪部分？

# request 2
你可以详细讲一下RMSD是怎么计算的吗

# reply 2
当然可以！我们来从**直观概念 → 数学表达 → 在蛋白质结构中的应用**，一步步讲清楚 RMSD 是怎么计算的。
 ### RMSD 是什么？（直观理解）
RMSD 衡量的是「两个结构中对应原子的空间距离有多接近」。
你可以把它想象成这样：
> 如果你把两个相似的积木模型叠在一起，RMSD 就是在这些积木点之间测的平均偏差。

假设你有两个结构，每个结构由 NNN 个原子组成，分别叫做结构 A 和结构 B。  
对应原子的位置是：
结构 A 的原子坐标：

$$ \vec{a}_1, \vec{a}_2, \ldots, \vec{a}_N $$


结构 B 的原子坐标：

$$ \vec{b}_1, \vec{b}_2, \ldots, \vec{b}_N $$


RMSD 的定义公式：
RMSD = sqrt( (1/N) * sum[i=1 to N] |aᵢ - bᵢ|² )
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjQ4NTk0OTY1LC0xMzIyMDM4MTQ1LC0xOD
k4NjA0ODQ1LDEzNTAyMzA3MzQsNjgzMzUwODU5LC0xMjg5Mjc4
NDEsLTE5OTg3MTM4MThdfQ==
-->