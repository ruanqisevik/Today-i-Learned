#iOS memory management (内存管理)

1. MRC(人工引用计数)

> MRC模式下，所有的对象都需要手动的添加retain、release代码来管理内存。使用MRC，需要遵守谁创建，谁回收的原则。也就是谁alloc，谁rel
ease；谁retain，谁release。
> 当引用计数为0的时候，必须回收，引用计数不为0，不能回收，如果引用计数为0，但是没有回收，会造成内存泄露。如果引用计数为0，继续释放，会造成野指针。为了避免出现野指针，我们在释放的时候，会先让指针=nil。

2. ARC(自动引用计数)

> ARC是IOS5推出的新功能，通过ARC，可以自动的管理内存。在ARC模式下，只要没有强指针（强引用）指向对象，对象就会被释放。在ARC模式下，不允许使用retain、release、retainCount等方法。并且，如果使用dealloc方法时，**不允许调用[super dealloc]方法**。



