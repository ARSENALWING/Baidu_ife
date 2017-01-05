# 百度前端技术学院任务  

##说明  
虽然百度前端技术学院的任务很久以前就结束了，但不失为一个很好的web前端的练习项目。  
目前暂定目标为完成第一阶段的任务，作为练习和检验HTML/CSS的学习成果。  
待日后学习完js以后，再尝试去完成后面的任务。  

##笔记
1、三栏式自适应布局方式  
1.1、自身浮动法  
左栏左浮，右栏右浮，中间栏通过设置margin撑开距离。**左栏和右栏标签需写在中栏标签前**，但该方法中间体容易受到clear:both属性影响。  
1.2、绝对定位法。  
左右栏用绝对定位固定在左右两边，中间栏通过设置margin撑开距离。**三个标签顺序不要求**，但当页面宽度较小时，会发生重叠。  
1.3、margin负值法。  
中间栏使用双层标签，外层宽度100%，并且浮动；内层设置margin撑开左右宽度。左栏左浮动，margin-left为-100%，右栏左浮动，margin-left为-200%。**需要写写中间栏标签，左右栏不要求**，这种布局放回不易受内部影响，但代码相对复杂，不方便排查。  

2、清除浮动
常见有clear、overflow和clearfix。clearfix为较优解决方案。  
```$xslt
.clearfix:after{
    content:".";
    display:block;
    height:0;
    clear:both;
    visibility:hidden
}
.clearfix{
    zoom:1;
}
```  
  
3、CCS3 calc()  
使用calc()可以方便的在ccs中进行一些简单的运算。  

4、background-position和background-size  
可以通过background-position控制背景的位置，属性的值有：  
（1）x，y坐标，单位有%和px；  
（2）left,right,center,top,bottom。可同时使用两个值进行描述，如left center，如只指定一个值，默认另一个值为center。