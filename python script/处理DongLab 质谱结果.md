
# request 1
之前你给我写过一个python脚本，如图所示，可以将表格中description列中的uniprot id提取出来。 我的表格有WormBaseID、Description、SQ Length、PSM Count、Coverage这几列，其中Description列中是对蛋白的描述，比较长的文本，比如“ CE15900 WBGene00001167 locus:eef-2 Elongation factor Tu family (contains ATP\/GTP binding P-loop) status:Confirmed UniProt:P29691 protein_id:CAB02985.1”。我想要把其中的uniprot ID提取出来成单独的一列，比如对于以上这个示例而言，我想提取“P29691”，放在新的一列中。 你之前给我的脚本（图1）已经可以比较好的完成这个任务，但是有个问题，Uniprot这一列中，每个uniprotID前面都会带一个“uniprot”这个词，如图2所示。我现在想要“干净的”Uniprot ID，只有字母数字前面不带东西。请你再图1脚本基础上改进，并说明为什么会出现这个问题。
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTU3NDQzOTQ3NywtMjA4ODc0NjYxMl19
-->