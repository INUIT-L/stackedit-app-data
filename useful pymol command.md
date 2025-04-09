> Written with [StackEdit中文版](https://stackedit.cn/).

# 收集的有用的pymol操作/命令
<br>
<br>


`set cartoon_oval_length, 0.6→设置α-螺旋的宽度；  # default is 1.2`
`set cartoon_oval_width , 0.2  # default is 0.25`

![oval length/width ](/imgs/2025-04-01/bHtEyzMhlu6XrrBV.png)



>Wizard→Measurement→点中要画的两个原子，形成相互作用；

## align对齐两个对象：

`align AF3gpr12model0, AF2gpr12, cycles=50 `


## Cartoon highlight color

This setting allows one to specify a contrasting color for the interior face of helices and the side faces of strands.
此设置允许指定螺旋内表面和股线侧面的对比色。
![输入图片说明](/imgs/2025-04-09/NFiRwviWFf7lHnqA.png)
```
set cartoon_highlight_color, grey
set cartoon_highlight_color, grey50   # sets cartoon highlight color to middle-grey
set cartoon_highlight_color, -1      # turns this feature off (default)
```

# transparency
单独的set transparency命令只是去调整surface和slices的透明度
**Transparency** is used to adjust the transparency of **Surfaces** and  **Slices** .
```
set transparency, 0.5
```

![输入图片说明](/imgs/2025-04-09/IFESN6gRQ0lXCCuM.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzNDc2NzcwMTUsNjc0NTYzMzU1LC0xNz
kyMjY4NjA2LDEzNDE1NjIwNjgsMjAzNjI1NTIxNyw5MDU0Njg4
OTEsLTgzNzA1MjAxMiwxMzg0NzU1MjM4LC01MjY1OTU1MF19
-->