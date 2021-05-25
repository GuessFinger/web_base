# web_base
html重新学习


- html
  hyper text markup language  超文本标记语言 是一种描述网页的语言
  html不是一种编程语言 而是一种标记语言
- web标准  就是为了让我们写的html能够没有差异化的展示  
  主要包括：结构(相当于骨头) 表现(我们的肉体啊，装饰之类的东西) 行为(行动，感性啊之类的操作)
  
  
- 
```html
   <!DOCTYPE> 文档类型 作用就是告诉浏览器使用哪种html版本来显式网页 因为有html5 html4 
   <!DOCTYPE html>·当前网页采用html5来显式网页
   <html lang="en">lang=zh-CN 语言种类描述
   <meta charset="utf-8"> 规定html应该采用哪种字符编码
   <strong>文件加粗标签</strong> <b>也是</b>
   <em>文本加粗标签</em> <i>也是</i>
   <del>删除线</del> <s>也是</s>
   <ins>下划线</ins> <u>也是</u> 
   <a href="http://www.baidu.com" target="_blank" >百度</a>  _blank 新打开一个页面
   <a href="#maodian">我们在合适的位置设置一个id 这样a标签就是访问到你设置的位置上</a>


   <!--
    针对table的
    align="center"  规定表格和其他元素的对齐方式
    border="1"  规定表格的单元格是否有宽度
    cellpadding="像素值" 规定单元格的边缘和内容之间的空白举例
    cellspacing="像素值" 规定单元格之间的空白距离
    
    rowspan="跨行合并单元格的个数"
    colspan="跨列合并单元格的个数"
    -->
    
    <!--  自定义列表   -->
    <dl>
        <dt>名词解释</dt>
        <dd>解释1</dd>
        <dd>解释2</dd>
        <dd>解释3</dd>
    </dl>   

   <!-- 表单就是为了收集数据的 -->     
   <!--    我们只要把鼠标放到用户名上  就可以进行输入信息了-->
    <label for="text">用户名：</label><input type="text" id="text">
    
    <!--  伪类  下面的伪类的书写顺序是有要求的  lv包包 hao   link visited hover active-->
    a:link  选择所有未被访问的链接
    a:visited 选择所有已经被访问的链接
    a:hover 选择鼠标指针位于其上的链接
    a:active 选择活动链接(鼠标按下未弹起的链接)

    input:focus  获取焦点后的元素样式

    元素的显式模式就是  元素标签以什么方式进行显示
    html元素一般分为 块元素和行内元素
   
    块级元素：h1 - h6  p  div ul ol li  div是最典型的块级元素
        1. 比较霸道 自己独占一行
        2. 高度 宽度 外边距以及内边距都可以进行控制
        3. 宽度默认是容器的100%(父容器的100%)
        4. 是一个容器及盒子 里面可以放行内或者块级元素
      注意：
        1. 文字类的元素内不能使用块级元素 p标签内不能再放置div元素  h也是一样的
    行内元素：a strong em ins del i span  span是电影的行内元素 行内元素也成为了内联元素
        1. 相邻的行内元素在一行上显式 可以显式多个
        2. 高和宽的设置是无效的
        3. 默认宽度就是它自己的宽度
        4. 行内元素只能容纳文本或者其他行内元素
       注意：
        链接内不能再放链接

```    

