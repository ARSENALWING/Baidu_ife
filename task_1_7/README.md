##关于第四部分下拉列表的说明  
代码中参考@vvvvip 团队的实现方法。  
1、创建三个与设计稿中下拉列表同样大小的单选按钮，
并通过设置z-index来使其至于最上层，并通过设置
不透明度为0来达到视觉上隐藏的目的。  
1、创建四个盒子，通过display:none;属性来隐藏创
建的下拉列表中的选择内容。调整位置到三个单选按钮
和确认按钮的上面。由于四个按钮为全透明，所以会显
示每个盒子的最顶部的没被隐藏的部位会视觉上显示出
来（实际上还是4个按钮在这4个盒子上层）。
3、通过设置当一个按钮为选中状态，改变对应的盒子
的下拉列表的display属性，使下拉列表显示出来。

在此感谢vvvvip团队对该问题解决的帮助！
附上原项目github：https://github.com/chenBuJuan/IFE-FirstStage-Task7


