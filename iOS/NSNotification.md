#NSNotification
- NSNotification继承自NSObject;
- 遵循NSCoding; NSCopying; NSObject;
- NSNotification对象本身携带信息, 所以它可以通过一个NSNotificationCenter对象广播消息至其他对象.   
 一个NSNotification对象(一个作为notification的返回对象)包含一个name, 一个object, 一个可选字典 dictionary.    
name是notification的标识.    
object是发送者希望传递给观察者的对象(典型的例子object即是发送通知的对象). 可选字典储存了其他相关的对象. 但即便如此NSNotification对象是一个不可变对象.

> # Creating Notifications
> \+ notificationWithName:object:   
> \+ notificationWithName:object:userInfo:    
> \- initWithName:object:userInfo: _(Designated Initializer)_
