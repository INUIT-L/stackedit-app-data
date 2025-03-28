
> Written with [StackEdit中文版](https://stackedit.cn/).
---

# Request1
我现在手里有一个fasta文件（“/Users/linjunxiang/Downloads/all_designs_full_seq.fasta”），里面的内容如图所示。首先是一个wt_full_seq.R的氨基酸序列。 下面是一些突变体的氨基酸序列（比如>GPR127y3g_design_9.R）。请你写一个python脚本，帮我达到以下目的，将每一个突变体的氨基酸序列和野生型的对比，识别出这个突变体中是哪个位点的氨基酸和野生型对比发生了突变，以及它突变成了哪个氨基酸。最后将他们整理到一个csv文件中。

# Repley1
你这个需求可以通过Biopython来处理FASTA文件，然后逐位比较每个突变体与野生型序列之间的差异。以下是一个完整的Python脚本，会输出一个CSV文件，列出每个突变体和其对应的突变信息（格式如：A123V，表示第123位从A突变为V）。
```python
# This is a comment
print("Hello, world!")
```




<!--stackedit_data:
eyJoaXN0b3J5IjpbMTk3NjYzNjU3OCwtMTcxMTcxNzU1LC05Nz
E5NjY3MzddfQ==
-->