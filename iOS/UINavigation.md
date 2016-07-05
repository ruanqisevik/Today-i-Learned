#UINavigation 导航控制器相关

###工作原理  
- `UINavigationController` 使用栈的方式管理导航控制器, 通过控制入栈和出栈来展示视图控制器
- `UINavigationController` 的 `ControllersView` 里始终显示栈顶控制器的`view`
- `viewControllers` 属性是导航控制器栈中所有控制器的数组集合
- `navigationController` 属性使得所有在栈中的控制器通过此属性获取到所在的`UINavigationController`对象􏰩􏱁􏳪   

###常用方法(In Swift)  
- `pushViewController(viewController: UIViewController, animated: Bool)`  
- `popViewControllerAnimated(animated: Bool) -> UIViewController?`  
- `popToViewController(viewController: UIViewController, animated: Bool) -> [UIViewController]?`  
- `popToRootViewControllerAnimated(animated: Bool) -> [UIViewController]?`  

###重要属性  
- `viewControllers`: 栈中所有控制器的数组集合
- `topViewController`: 位于栈顶的控制器
- `visibleViewController`: 正在显示的控制器
- `navigationBar`: 导航栏  
- **`navigationBarHidden`**: 与 `navigationBar.hidden` 类似, 当此属性为 `true` 时, `navigationBar` 隐藏, 但不同的是此时屏幕左边缘右划 pop 返回的动作也被禁用, 而 `navigationBar.hidden` 动作不失效    

#####导航栏
- `translucent`: 导航栏是否透明 (当 `translucent` 为 `true` 时, `contentView` 会被 `navigationBar` 覆盖一部分, 反之, 则 `contentView` 会从 `navigationBar` 底部开始展示 )  
- `tintColor`: 影响到 `navigationBar` 的各项 `Item` (疑问: 是否区别于 iOS7 后出现的 `view` 的 `tintColor` 属性?)
- `barTintColor`: 区别于 `tintColor`, 可以用来设置 `navigationBar` 的背景色  
- `shadowImage`: 导航栏下沿的阴影图片 注意:For a custom shadow to be shown, a custom background image must also be set with -setBackgroundImage:forBarMetrics: (if the default background image is used, the default shadow image will be used).  

#####UIBarButtonItem
可以设置用来替代系统自带的返回键, 需要注意的是, 利用 `leftBarButtonItem` 作为返回按钮时, 需要自己制定 button 的点击事件. 对于navigation侧滑返回手势可能失效的问题,可以尝试添加`self.navigationController.interactivePopGestureRecognizer.delegate = (id)self`;
