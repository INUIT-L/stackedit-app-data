> Written with [StackEdit中文版](https://stackedit.cn/).

# 收集的有用的pymol操作/命令
<br>
<br>


## 调整α-螺旋的宽度
```
set cartoon_oval_length, 0.7  # 设置α-螺旋的宽度；  # default is 1.2
set cartoon_oval_width , 0.2  # default is 0.25
```
![oval length/width ](/imgs/2025-04-01/bHtEyzMhlu6XrrBV.png)

<br>
<br>

## align对齐两个对象：
以[AF2](https://github.com/INUIT-L/stackedit-app-data/blob/master/PDB/practice/AF2gpr12.pdb) / [AF3](https://github.com/INUIT-L/stackedit-app-data/blob/master/PDB/practice/AF3gpr12model0.pdb)预测的GPR12为例子。

```
先把两个结构拖进pymol
调整颜色
set cartoon_oval_length, 0.7
align AF3gpr12model0, AF2gpr12, cycles=50 
这样之后直接ray的细节效果如左下

set cartoon_highlight_color, -1
set ambient, 0.4
set specular, 0（似乎没影响）
set ray_trace_depth_factor, 1
set ray_trace_disco_factor, 1
set ray_trace_mode, 1
set antialias, 2
set ray_shadow, off
用滚轮调整虚实，之后ray，如右下
```

<p float="left">
  <img src="/imgs/2025-04-10/JEpUX91EzXf6WNqA.png" width="300"/>
    <img src="/imgs/2025-04-10/1PGuIAZWfcrqZks0.png" width="300"/>
</p>


<br>
<br>


## Cartoon highlight color

This setting allows one to specify a contrasting color for the interior face of helices and the side faces of strands.

<img src="/imgs/2025-04-09/NFiRwviWFf7lHnqA.png" width="400" alt="cartoon_highlight"/>

```
set cartoon_highlight_color, grey
set cartoon_highlight_color, grey50   # sets cartoon highlight color to middle-grey
set cartoon_highlight_color, -1      # turns this feature off (default)
```

<br>
<br>

## transparency
### Whole Surface
单独的set transparency命令只是去调整surface和slices的透明度，
比如我参照小红书[“如何绘制残基相互作用图”](https://www.xiaohongshu.com/user/profile/62e4d86a000000001e01d536?xsec_token=ABLNzGWkdT0ygIOPLvu5WINMnyhNmbATmIkw0WuWHs4LY=&xsec_source=pc_collect)教程中所示的：
```
fetch 7y3g
CmdLoad: "./7y3g.cif" loaded as "7y3g".
Setting: bg_rgb set to white.   #设置背景颜色为白色
Setting: opaque_background set to on.
通过chain 选中GPCR，右键 action → extract object → 将GPCR提取为一个新的object
剩下的7y3g部分，action → delete object
修改GPCR的颜色，改成lightblue，然后点击all右侧的S > surface
set transparency, 0.8  # show all surfaces with 80% transparency.
可以得到如左图的结果。 直接 set ray_trace_mode, 1，得到中图的结果。

在中图的基础上，
set ray_shadow, off
set antialias, 2
set ray_trace_depth_factor, 1
set ray_trace_depth_factor, 1
set specular, 0
set ambient, 0.4
ray
得到右图的结果
```
<p float="left">
  <img src="/imgs/2025-04-09/8rwIx5xo0DVrMmaS.png" width="300"/>
  <img src="/imgs/2025-04-09/1nC3Q2VOcVz2nE0n.png" width="300"/>
  <img src="/imgs/2025-04-09/T4mcGeLIMvlCFOgU.png" width="300"/>
</p>


### Selected Surface Elements
```
fetch 7y3g	# 加载蛋白 GPR12-GsGβGγ-Nb35 complex（刘志杰组）
改变颜色：color-by chain-elementC
set transparency, 0.65, chain R		#将chain R (GPCR)的透明度变成0.65
set transparency, 1, chain R		#将chain R (GPCR)的透明度变成1(完全透明)
set transparency, 0, chain R		#切换选择模式时，先手动还原上一步的操作，这里选择chain R变到选择chain R中的氨基酸
set transparency, 0.65, chain R and resi 1-100		#将chain R的1-100个残基的surface变成透明
set transparency, 0.65, chain R and i. 1-100	# resi 1-100和i. 1-100是等价的, i.是resi的aliase
```
<p float="left">
<img src="/imgs/2025-04-10/18I5mQRWzrWVrSke.png" width="300"/>
<img src="/imgs/2025-04-10/cJKoLjLYsqfG7jwa.png" width="300"/>
<img src="/imgs/2025-04-10/NzYWb0zF9ys78uw8.png" width="300"/>
</p>

### Cartoon transparency
第一次知道cartoon transparency是因为，想要绘制如下的结构图，其中整体的结构没有轮廓线，突出的氨基酸和配体有轮廓线。
<img src="/imgs/2025-04-10/nBEQo7elx3ooAiia.png" width="300"/>
请教小红书之后得到以下答复：
>ray_trace_mode设成1，然后给蛋白质设个看不出来的透明度，比如set cartoon_transparency, 0.05，最后ray一下。有透明的结构在ray的时候就不会有轮廓

```
fetch 8kh5		# 自己组的GPR174 bound to LysoPS 结构
b
把GPR174 extract出来
#
```
<p float="left">
<img src="/imgs/2025-04-10/lWXvUS9Vm2f7WQez.png" width="300"/>
<img src="/imgs/2025-04-10/XSeujx1CnUTp2xwX.png" width="300"/>
<img src="/imgs/2025-04-10/tyaPnhNqlXtfhrjW.png" width="300" />
</p>







### 其他
Wizard→Measurement→点中要画的两个原子，形成相互作用；





<!--stackedit_data:
eyJoaXN0b3J5IjpbNDQ2NDMxMDY0LC03MDY5NzgxODMsMTU3ND
U0ODU1OCw1MTkzNDA3MTgsLTExNDEyMTk4NjIsMTQ4ODI1ODgy
OSwtMTAyMjIwNTY5MCwxNjk1NjcxODA5LDE4ODA2MDEwNSwxNT
U0NjU0NTU0LC0yMzExMTc1NDAsMTYzMTUwNTg0OSwtMTg1OTQx
MzUxMywtOTY3MjY0NzU4LC01NjY4ODU0MTIsLTE0Njg1NDEyNj
ksLTEzMDk2NDYyMTEsLTIzMDQyNzY1MiwtMjA2NjM3MzI5OCw5
OTg4NjAyMDZdfQ==
-->