#### Android

1. MVC 、 MVP 、 MVVM ?

   - MVC: View 持有了Controller，把事件传递给Controller，Controller 由此去触发Model层的事件，Model更新完数据（网络或者本地数据）之后触发View的更新事件

   ![MVC.png](https://upload-images.jianshu.io/upload_images/2376645-920ecb14e5f74278.png)

   - MVP: 

     MVP演化自MVC，View只专注于视图的更新操作，Presenter用于沟通View和Model之间的联系，Model只进行数据操作而不直接进行View的更新。Model数据操作完成后由Presenter通知View刷新数据

     优点：MVP模式会解除View与Model的耦合，避免业务逻辑被塞进View中

     缺点：

     ​	1.Presenter层与View层关系太紧密，可能造成View层修改Presenter层跟着修改的局面

     ​	2.传统的MVP需要创建太多的类和接口

     ​        3.为了处理第二点，可能会重用Presenter，可是如要重用presenter可能会实现过多不需要的接口，处理这过多接口的问题可以尝试使用handlerMessage方式，

     ​		具体可学习下： https://www.jianshu.com/p/ac51c9b88af3

   ![MVP.png](https://upload-images.jianshu.io/upload_images/2376645-8d8bac1ac5f50b59.png)

   - MVVM: 又称状态机制，View和ViewModel 是双向绑定的，改变ViewModel会直接作用到View视图上，而View会把事件传递给ViewModel，ViewModel去对Model进行操作并接受更新。

   ![MVVM.png](https://upload-images.jianshu.io/upload_images/2376645-66197c4cd472faf2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/434)

   

   - MVPVM：MVP加入了ViewModel之后的变种，在MVP的基础上加入ViewModel做View与Model之间的数据绑定，用处暂时未知

2. 

3. 