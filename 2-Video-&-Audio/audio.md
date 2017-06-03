# 音频audio
H5新特性——音频播放
  H5提供了一个新的标签用于播放音频：
	<audio src="res/bg.mp3"></audio>
	<audio>
    		<source src="res/bg.mp3">
    		<source src="res/bg.ogg">
    		<source src="res/bg.wav">
    		您的浏览器不支持AUDIO播放！
  	</audio>
  它默认是一个300*30的inline-block元素；但若没有controls属性，则display:none。
  AUDIO标签/对象常用的成员：
  成员属性：
	autoplay：false，是否自动播放
	controls：false，是否显示播放控件
	loop：false，是否循环播放
	muted：false，是否静音播放
	preload：视频的预加载策略，可取值：
		auto：预加载视频的元数据以及缓冲一定时长
		metadata：仅预加载视频的元数据(尺寸、时长、第一帧内容)，没有视频缓冲
		none：不预加载任何数据
     -------------JS对象属性---------------------
	currentTime：当前播放的时长
	duration：总时长
	paused：true，当前视频是否处于暂停状态
	volume：1，当前音量
	playbackRate：1，回放速率，大于1表快放，小于1表慢放
  成员方法：
	play( )： 播放视频
	pause( )： 暂停播放
  成员事件：
	onplay：	当视频开始播放时触发的事件
	onpause：当视频开始暂停时触发的事件

练习：使用复选框控制网页背景音乐