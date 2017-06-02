# HTML5 demos
### HTML5中表单的新特性
  #### (1)新的input type  	<input type="?">
	H4中的input type：text、password、radio、checkbox、file、hidden、submit、reset、image
	H5中的input type：email、url、number、tel、search、range、color、date、month、week
 #### (2)新的表单元素
	H4中的表单元素：input、textarea、select/option、label、button(默认type是submit)
	H5中新增的表单元素：datalist、progress、meter、output
  #### (3)表单元素的新属性
    1）placeholder 占位字符、
    <input value="tom" placeholder="请输入用户名">，与value不同，不能用于提交
      placeholder="提示性文字"
    2）autofocus 自动获取输入焦点、
    <input autofocus>
      autofocus页面上只要一个，但如果有两个时，默认第一个自动获取焦点
      在js对象中其值默认为false
    3）multiple 允许输入框中出现多个输入（用逗号分隔），一般需要和特殊的输入组合使用，如邮箱输入域，url等、
    <input type="email" multiple>
    4）form 用于把输入域放置到FORM外部、
    <form id="f5"></form>
    	  <input form="f5">
          在js对象中其值默认为“”，空字符串
     在input中用form属性指定所属的表单的id，哪个input要提交，谁添加form属性
  	5）required 必填项，内容不能为空、
  	<input required>
  	6)maxlength：指定字符串的最大长度
    <input maxlength="9">，超过9就不让输入
    7)minlength：指定字符串的最小长度
    <input minlength="6"> 有输入的条件下minlength才生效，所有最好搭配required一起使用
    8)max：指定数字的最大值
   	<input max="60">
    9)min：指定数字的最小值
    <input min="18">
    10)pattern：指定输入必需符合的正则表达式
    <input pattern="^1[35789]\d{9}$">   ^$可以省略不写
      只在有输入的情况下才生效，所有与require搭配使用
    <input type="tel"/>，基本废物，不会有验证
         以上6个在真正项目中基本不怎么用，样式太丑，不能自定义
    上述验证属性会影响表单元素对应的JS对象的validity属性。
 #### (4)H5新增与验证相关的JS对象级属性
    input.validity {	        //输入框的验证有效性
  	badInput:false		//无效的输入，如number输入字母
  	customError:false	//存在自定义错误
  	patternMismatch:false	//不匹配指定的正则表达式
  	rangeOverflow:false	//值上溢出
  	rangeUnderflow:false	//值下溢出
  	stepMismatch:false	//步长不匹配
  	tooLong:false		//内容太长
  	tooShort:false		//内容太短
  	typeMismatch:false	//类型不匹配
  	valueMissing:false	//值缺失
  	valid:true		//当前输入值有效
  }
