2019-5-7:<br>
scrollView,滑动需要设置contentSize<br>
浏览器卡顿原因，浏览器本身卡顿（急速模式和兼容模式），网络拥塞，网页服务器响应延迟。用IE来作为基线进行测试<br>
<br>
2019-5-9:<br>
iOS访问本地相册，使用UIImagePickerController,设置属性sourceType为UIImagePickerControllerSourceTypePhotoLibrary,遵守协议<UIImagePickerControllerDelegate, UINavigationControllerDelegate>, 实现代理方法didcancel和didfinishpicking（偷懒简写）<br>
tableview有显示但是无响应<br>
原因：你的tableView超出View的边界，即你添加的tableView视图在父视图边界之外，但是是默认可以显示。事件响应机制里有：超出边界部分不响应事件<br>
解决方法：在父视图中重写hittest<br>
<br>
2019-5-10<br>
子视图的frame超出父视图的frame，需重写父视图的hittest方法。<br>
NSDictionary是不可变字典，创建时就确定值，创建完成不可修改其值<br>
<br>
2019-5-14<br>
修改导航栏标题，使用vc.navigationItem.title=@""，其中vc是视图控制器<br>
<br>
2019-5-20<br>
进入BIOS – Security – Secure Boot Control设为Disabled。<br>
进入BIOS – Boot – Lunch CSM设为Enabled。然后按F10保存退出。<br>
<br>
华硕主板自带一个软件，Q-installer，自带网卡驱动，以及自动下载集成在主板上的其他硬件驱动<br>
<br>
2019-5-21<br>
奇怪的事件之UIButton和tap手势优先级 <br>
模拟器---根视图控制器是UITabbarController,加入了tap手势，在其中一个tab视图下有UIButton按钮，点击按钮，先触发的是按钮事件，后触发手势事件<br>
按照苹果官方说明文档，应该是手势的优先级大于responder
<br>
<br>
2019-5-22<br>
win10系统10240版本无法更新<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
