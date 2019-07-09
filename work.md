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
2019-5-24<br>
ios NSDictionary 存储无法识别的类型时，会断点报错。当接受从网络端发来的消息时需要注意，可以让后台修改返回数据类型<br>
<br>
2019-5-29<br>
iOS， 网络请求是异步执行。viewdidload和viewwillappear和viewdidappear顺序执行，无论在那个方法内进行网络请求，都不会阻塞这三个方法执行<br>
懒加载， <br>
```
-(nsstring *)mystring{
    if(!_mystring)
    {
        _mystring=[[nsstring alloc] init];
    }
    
    return _mystring;
}
```
<br>
2019-6-3<br>
用Cocos creator打包的iOS，注意初始场景要选好。然后是设置launchimage，需要用真机测试，要不然在测试机上一直显示cocos默认的图标<br>
<br>
2019-6-4<br>
ios的线程，分4种，分别是pthread，nsthread， GCD， NSOperation。这里要注意的是，如果有使用nsurlsession实现网络方面的功能， 则在创建线程时需要使用第四种方法， 因为nsurlsession的一个方法里有使用NSOperation相关的作为参数， 使用NSOperation可以配置该方法在那个线程中执行<br>
<br>
2019-6-5<br>
在使用通知的时候，需要确定接收通知是否会进行UI操作，如果需要操作UI，则必须在主线程发送通知<br>
<br>
2019-6-6<br>
创建视图之后，如果数据更新了，记得要‘刷新’一下视图。比如tableview，数据有更新，那就需要使用reloaddata<br>
<br>
2019-6-10<br>
nsmutabledictionary有一个实例方法addEntriesFromDictionary，是从一个字典拷贝所有值到另一个字典.nsdictionary在初始化时，使用initwithdictionary也可以达到同样的效果<br>
<br>
2019-7-9<br>
系统装完后会缺少c++运行库，部分软件依赖这个库，需要去下载微软的基础运行库<br>
英伟达显卡驱动，里头有个软件，CTRL+alt+z可以呼出，这个软件和ps的快捷键有冲突，且会造成右下角的遮挡（一个麦克风图标和一个刷新图标）<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
