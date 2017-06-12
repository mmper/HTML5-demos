# HTML5高级新特性---SVG

### SVG绘图
* Scalable Vector Graph：可缩放的矢量图
	            Canvas绘图	                    SVG绘图
    类型	        2D位图	                        2D矢量图
    放大      	失真      	                    不会失真
    如何绘图	    使用JS代码绘图	                使用标签/元素绘图
    事件绑定	   每个图形不是元素，无法直接绑定事件	每个图形都是元素，可以直接绑定事件监听
Web项目应用场合	统计图、游戏、(渐变)	            统计图、图标、地图

* 使用SVG进行绘图——矩形
  <rect width="" height="" x="" y="" fill="" fill-opacity="" stroke="" stroke-width="" stroke-opacity=""></rect>
* 使用SVG进行绘图——圆形
  <circle r="" cx="" cy="" fill="" fill-opacity="" stroke="" stroke-opacity=""></circle>
* 使用SVG进行绘图——椭圆
  <ellipse rx="" ry="" cx="" cy="" fill="" fill-opacity="" stroke="" stroke-opacity=""></ellipse>
* 使用SVG进行绘图——直线
  <line x1="" y1="" x2="" y2="" stroke="" stroke-width="" stroke-linecap="butt/square/round"></line>
stroke-linecap（指定线头的样式）="  butt:   默认，向线条的每个末端添加平直的边缘
                                  square: 向线条的每个末端添加正方形帽子，会比butt导致线变长
                                  round:  向线条的每个末端添加圆形的帽子

提示：若多个SVG图形有完全一样的属性，可以抽出来，放在一个公共的父元素中（小组）
使用<g></g>创建标签组，本身不可见，但可以用来盛放子元素，保存多个子元素公用的的属性，子元素会继承
<g stroke="#000">
   <line></line>
   <line></line>
</g>
* 使用SVG进行绘图——折线
  <polyline points="50,50  100,300 ..." fill="transparent" stroke="#000"></polyline>
* 使用SVG进行绘图——多边形
<polygon points="50,50  100,300 ..." fill=""></ polygon>
* 使用SVG进行绘图——文本
  <text font-size="" alignment-baseline="before-edge" fill="" stroke="" x="" y="">文本内容 </text>
* 使用SVG进行绘图——图像
  不能使用IMG置于SVG画布上！只能使用：
  &lt;image xlink:href="disc.png" width="200" height="200" x="" y=""&gt;

网页中可用的绘图技术：
(1)Canvas绘图 --H5新增的原生技术，是一种2D JS位图绘图技术
(2)SVG绘图 --H5采纳的已有技术，是一种2D 标签 矢量图绘图技术
(3)WebGL绘图 --尚未采纳为H5标准，是一种2D/3D JS绘图技术，具体可参考three.js

