# fed-e-task-01-01
fed-e-task-01-01
1.CD
2.ABC
3.
1）patchVnode会在对比新旧两个节点之前触发prepatch和update钩子函数
2）新节点是否有text属性且不等于纠结点的text属性，如果是，要去更新老节点DOM的内容，如果老节点有children，则会调用removeVnodes移除对应的DOM元素并设置新DOM的textContent 
3）如果新老节点都有children,则会对比，若不相等，则调用updateChildren,更新差异
4）如果新节点有children,且老节点没有，并且老节点有text属性，则需要先清除老节点的textContent，并添加对应的子节点
5）如果老节点有children，而新节点没有，则移除所有的老节点
6）如果老节点有text，而新节点没有，则清空老节点的textContent
7)出发postpatch钩子函数
