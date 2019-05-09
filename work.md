2019-5-7:<br>
scrollView,滑动需要设置contentSize<br>
浏览器卡顿原因，浏览器本身卡顿（急速模式和兼容模式），网络拥塞，网页服务器响应延迟。用IE来作为基线进行测试<br>
2019-5-9:<br>
iOS访问本地相册，使用UIImagePickerController,设置属性sourceType为UIImagePickerControllerSourceTypePhotoLibrary,遵守协议<UIImagePickerControllerDelegate, UINavigationControllerDelegate>, 实现代理方法didcancel和didfinishpicking（偷懒简写）<br>
tableview有显示但是无响应
原因：你的tableView超出View的边界，即你添加的tableView视图在父视图边界之外，但是是默认可以显示。事件响应机制里有：超出边界部分不响应事件
