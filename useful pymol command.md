> Written with [StackEdit中文版](https://stackedit.cn/).

# 收集的有用的pymol操作/命令
<br>
<br>


## 调整α-螺旋的宽度
`set cartoon_oval_length, 0.6  # 设置α-螺旋的宽度；  # default is 1.2`
`set cartoon_oval_width , 0.2  # default is 0.25`

![oval length/width ](/imgs/2025-04-01/bHtEyzMhlu6XrrBV.png)
<br>
<br>

## align对齐两个对象：

`align AF3gpr12model0, AF2gpr12, cycles=50 `
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

# transparency
单独的set transparency命令只是去调整surface和slices的透明度
比如我参照小红书[“如何绘制残基相互作用图”](https://www.xiaohongshu.com/user/profile/62e4d86a000000001e01d536?xsec_token=ABLNzGWkdT0ygIOPLvu5WINMnyhNmbATmIkw0WuWHs4LY=&xsec_source=pc_collect)教程中所示的：
```
fetch 7y3g
CmdLoad: "./7y3g.cif" loaded as "7y3g".
Setting: bg_rgb set to white.   #设置背景颜色为白色
Setting: opaque_background set to on.
通过chain 选中GPCR，右键 action → extract object → 将GPCR提取为一个新的object
剩下的7y3g部分，action → delete object
修改GPCR的颜色，改成lightblue，然后点击all右侧的S > surface
set transparency, 0.8
可以得到下图的结果
```
<img src="/imgs/2025-04-09/8rwIx5xo0DVrMmaS.png" width="300" alt="GPCR_transparency"/>

<img src="/imgs/2025-04-09/BW0Zx6LFD1SVvJni.png" width="300" alt="GPCR_transparency"/>


<img src="/imgs/2025-04-09/IFESN6gRQ0lXCCuM.png" width="400" alt="cartoon_highlight"/>



>Wizard→Measurement→点中要画的两个原子，形成相互作用；
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMjYyOTA3NDQsLTE4MDM3OTMyNzUsMT
M2ODI1MTcwNiwxOTk2MjQ1NjkwLDcxMzg1NTY5Myw2NzQ1NjMz
NTUsLTE3OTIyNjg2MDYsMTM0MTU2MjA2OCwyMDM2MjU1MjE3LD
kwNTQ2ODg5MSwtODM3MDUyMDEyLDEzODQ3NTUyMzgsLTUyNjU5
NTUwXX0=
-->