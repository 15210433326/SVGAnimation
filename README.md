# SVGAnimation
Jquery包装的控制Flash导出的SVG的动画播放
如有疑问或者Bug 请与我联系  qq452202586



先说以下原理：
  通过导出SVG可获取每个DOM的Matrix数据，通过倒出方式获取每个关键帧的MAtrix数据
  确定总帧数
  然后通过每个关键帧计算出具体每帧的变化值
  然后计算出所有帧的Matrix数据
  
  通过requistAnimationFrame来刷新动画播放


首先需要通过FLash或者Ai制作SVG的，这里以Flash cc2014为例，对当前关键帧的元件进行命名
然后通过  文件－－－导出－－－图像（选择SVG），选择“嵌入”，然后点击保存。

API包括
zdw_init(_key_Frames,total_frame) 
构造函数 返回实例化对象。
初始化动画数据（关键帧的数据对象，总帧数）

gotoAndPlay（num，loop）
方法

gotoAndStop（num）
方法

fromAndPlay（start，end）
方法：从某一帧到某一帧播放动画，可用于倒放

stop（）
方法

play（）
方法

-------------------------------------------------
属性

loop  是否循环

curFrame   当前帧数

totalframe   总帧数

