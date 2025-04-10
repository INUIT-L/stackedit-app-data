> Written with [StackEdit中文版](https://stackedit.cn/).



## Selection Algebra

PyMOL's selection language allows to select atoms based on identifiers and properties. Many commands (like [color](https://pymolwiki.org/index.php/Color "Color"), [show](https://pymolwiki.org/index.php/Show "Show"), etc.) take an atom selection argument to only operate on a subset of all atoms in the scene. Example:
```
PyMOL>show spheres, solvent and chain A
```

Selections can be made more precise or inclusive by combining them with logical operators, including the boolean and, or, and not. The boolean and selects only those items that have both (or all) of the named properties, and the boolean or selects items that have either (or any) of them.

![输入图片说明](/imgs/2025-04-10/q3WstvnGNMaQmaTT.png)
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE5NTAzMzQ3LC0yMDkwMTA2MjFdfQ==
-->