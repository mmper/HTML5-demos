# 视频video
H5提供了一个新的标签用于播放视频：
	第一种：<video src="res/birds.mp4"></video>
	第二种：解决浏览器不支持问题，写三种。。MP4/ogg/webm（转换：下载格式工厂），一般都支持MP4
<video>
    		<source src="res/birds.mp4">
    		<source src="res/birds.ogg">
    		<source src="res/birds.webm">
    		您的浏览器不支持VIDEO播放！
  	</video>
老浏览器不支持video标签，不认识就直接忽略这个标签，只解析文字，
所以可以在video中写一段文字：您的浏览器不支持VIDEO播放！
支持video标签时，video中的文字不认
  它本身是一个300*150的inline-block元素。若指定了src视频源，会自动用第一帧的宽高撑开行内块元素。
  要实现居中：给父级元素加text-align:center;

VIDEO标签/对象常用的成员：
  成员属性：播放控件
	autoplay：false，是否自动播放
	controls：false，是否显示播放控件
	loop：false，是否循环播放
	muted：false，是否静音播放
	poster：''，在播放第一帧之前显示的海报（音频没有，其他一样）
	preload：视频的预加载策略，可取值：
		auto：预加载视频的元数据以及缓冲一定时长
		metadata：仅预加载视频的元数据(尺寸、时长、第一帧内容)，没有视频缓冲
		none：不预加载任何数据
     ---JS对象专有属性---原生JS专用------------------
	currentTime：当前播放的时长
	duration：总时长
	paused：true，当前视频是否处于暂停状态
	volume：1，当前音量。1为100%，可以在script中自定义 x.volume=.5; 用定时器配合，可达到音量淡入淡出
	playbackRate：1(默认)，回放速率，大于1表快放，小于1表慢放
  成员方法：
	play( )： 播放视频
	pause( )： 暂停播放
  成员事件：
	onplay：当视频开始播放时触发的事件
	onpause：当视频开始暂停时触发的事件

	练习1：不使用Video自带的controls，自定义播放/暂停按钮

        	鼠标移出视频区域，隐藏按钮；鼠标移入，显示按钮
        练习2：不论何种原因，只要视频暂停(如点击暂停按钮、播放完毕、缓冲不足等)，就显示一副广告；只要播放，就隐藏广告

        	提示：必须监听视频的onplay和onpause事件