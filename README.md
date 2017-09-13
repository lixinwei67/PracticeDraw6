![](images/icon.png)

HenCoder 绘制 6 属性动画 练习项目
===

### 这是什么？

这不是一个独立使用的项目，它是 [HenCoder Android 开发进阶：UI 1-6 属性动画（上手篇）](http://hencoder.com/ui-1-6) 的配套练习项目。

### 怎么用？

项目是一个可以直接运行的 Android App 项目，项目运行后，在手机上打开是这样的：

![](images/preview.png)

工程下有一个 `/practice` 目录：

![](images/project_practice.png)

你要做的是就是，在 `/practice` 下的每一个 `PracticeXxxView.java` 文件中写代码，绘制出和页面上半部分相同的效果。就像这样：

![](images/preview_after.png)

> 当然，没必要做得和示例一毛一样。这是一个练习，而不是一个超级模仿秀，关键是把技能掌握。

如果做不出来，可以参考 `/sample` 目录下的代码：

![](images/project_sample.png)

练习做完，这期的内容也就掌握得差不多了。


1. View.animate() 方法会返回 ViewPropertyAnimator 对象，可以直接对 View 进行动画
2. ViewPropertyAnimator 可以同时执行一系列动画(Translation/Rotation/Scale/Alpha)
3. ObjectAnimator 可以执行 ViewPropertyAnimator 无法实现的动画，但是需要在自定义 View 中对需要改变的属性添加 setter/ getter 方法，因为 ObjectAnimator 就是调用 target 的属性的 setter 方法来改变，另外，如果没有指定动画的初始值，还会调用 getter 方法来获取当前值作为初始值