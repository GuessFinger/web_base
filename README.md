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
    cellpadding="像素值" 规定单元格的边缘和内容之间的空白距离
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
     如果我们想要把块级元素变成行内元素  display:inline 如果我们想要把行内元素变成快级元素的话 display:block

     经常在项目中 我们需要使用到文字的居中  让文字的行高等于盒子的高度 line=height

     background-position 访问名词   center top 

    css的三大特性 层叠性 (就是相同的样式会被覆盖，以离得近的为准) 继承性（就是你给父用户设置样式是可以继承的） 优先性
    
    后续如果有元素继承了body的font属性 后面的1.5 表示的就是当前元素的字体大小的1.5倍 就是当前元素的行高
    body {
      font:12px/1.5         
    }

    选择器权重

    继承或者 *                      0,0,0,0
    元素选择器                      0,0,0,1
    类选择器，伪类选择器             0,0,1,0
    id选择器                        0,1,0,0
    行内选择器                      1,0,0,0
    !important 重要的               无穷大

    复合选择器会有权重叠加的问题   最后li的颜色就是pink
    它的权重是 0,0,0,1 + 0,0,0,1 
    ul li {
      color: green      
    }
    它的权重是0,0,0,1  
    li {
      color: red
    }
    它的权重是 0,0,1,0 + 0,0,0,1
    .nav li {
      color: pink
    }
    这个问题确实没有注意过  还有需要注意 继承的权重是0

    盒子模型  外边距margin 边框border  内边距padding  内容content
    border : 2px solid red
        针对表格 如果设置边框的话 两个边框会进行重叠的 可以设置 border-collapse:collapse  合并相邻的边框 它会影响盒子的实际大小

    padding 内边距 也就是边框和内容之间的距离   如果设置了padding的话  div原来的宽度是200*200 设置了padding 20  盒子会被撑大
      就会变成 240*240  它会影响盒子的大小 
      在做导航栏的时候  我们可以不设置width  直接设置padding-left  padding-right  这样的话，会根据内容进行能自动调整
      如果不指定宽度的话  padding不会撑开盒子
    margin  指定盒子与盒子之间的距离
      外边距可以让块级盒子水平居中显式 但是必须满足两个条件   盒子P必须指定width  盒子的 左右 边距都设置为auto

      1. 相邻元素块垂直外边距合并问题
        a  margin-bottom 20px
        b  margin-top 10px
        a 和 b 垂直排列  按照常理说 他们直接的间距应该是30px  实际的应该是取两个值中较大的一个 相邻块元素垂直边距合并 如果想要解决这个问题   直接给一个盒子添加margin就好了
      2. 嵌套块元素垂直外边距的塌陷问题
        a   margin-top 50px
        b   margin-top 80px
        a 是 b 的父亲  想的是 b 在 a 容器里面  top 80px  实际上  a 直接 margin-top 80px
        <div style="width: 200px;height: 500px;background: red;">
          <div style="width: 120px;height: 250px;background: burlywood;"></div>
        </div>
        想要解决这个问题  
        - 给父元素  定义上边框
        - 给父元素  定义上边距
        - 可以为父元素添加 overflow:hidden

        行内元素我们尽量只设置 左右内外边距  

        有一些元素自带一些内外边距  可以使用 
        *{
            margin:0
            padding:0
        }

        ul>li  如果想要去掉li前面的小圆点  
        li {
          list-style:none          
        }

        盒子阴影
        h-shadow   Horizontal  水平阴影
        v-shadow   vertical   垂直阴影

        text-shadow  我们这样设置就是文字阴影

       网页布局的本质 用css摆放盒子 把盒子摆放到合适的位置

       浮动特定
        1. 脱离标准流的控制 移动到指定的位置 
        2. 浮动的盒子不再保留原来的位置
        3. 如果多个盒子都设置了浮动 则它们会按照属性值一行内显式并且顶端对齐
        4. 任何元素都可以进行浮动 不管原先是什么模式的元素 添加浮动后具有行内块元素相似的特性



```    

