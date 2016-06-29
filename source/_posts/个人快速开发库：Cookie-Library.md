title: 个人快速开发库：Cookie-Library
date: 2016-06-22 11:26:58
tags:
  - Android
  - 快速开发
categories:
  - Android 平凡之路
---

## 前言
前前后后做了安卓开发也有些日子，但是唯一遗憾的是还没能做出什么像样的个人作品，虽然零零散散的倒是有那么几个。

现在总结自己开发的习惯，把自己常用的开发库和一些自己整理的工具类、自定义控件，一些基本类的基类等整合起来，做成一个快速开发库，供以后使用。虽说是自己用的，当然，如果你也感兴趣，也可以试试看，在使用过程中有什么好的建议，也欢迎互相交流。

那么，接下来就开始简单的介绍一下这个库吧。

<!-- more -->

## 库结构图
![cookie-library](http://7xt6qm.com1.z0.glb.clouddn.com/Cookie-Library_201606291.png)

## 库结构介绍
整个库的名字叫做cookie-library，整个结构包括了Activity，Adapter，Application，Fragment，Interface，NetWork，Utils，Widget。

### Activity
- BaseActivity：Activity的基类
- BaseFragmentActivity：FragmentActivity的基类

### Adapter
- CommonAdapter：万能适配器
- CommonViewHolder：配合万能适配器使用的ViweHolder
- CommonRecyclerAdapter：RecycleView的通用适配器
- CommonRecyclerViewHolder：配合RecycleView通用适配器的ViewHolder
- OnRecyclerItemClickListener：RecycleView通用适配器的点击监听器接口
- RecycleViewDivider：RecycleView的分割线

### Application
- ActivityCollections：Activity的堆栈管理类
- BaseApplication：Application的基类

### Fragment
- BaseFragment：Fragment的基类

### Interface
- CallBack：在使用MVP架构的时候使用的回调

### NetWork
- NetChangeCallBack：网络状况发生改变时的回调接口
- NetStatusReceiver：网络状态监听广播接收器

### Utils
- KeyBoardUtils：软键盘打开关闭工具类
- LogUtils：日志工具类
- NetUtils：网络状况获取相关工具类
- PicCompressUtil：图片压缩工具类
- ProgressUtils：显示ProgressDialog的工具类
- RegexValidateUtils：正则表达式表单验证工具类
- ScreenUtils：屏幕相关工具类，可以获取屏幕宽高度，还有截取屏幕
- SDCardUtils：SD卡相关功能辅助类
- SharedPreferencesUtils：SharedPreferences工具类
- TimeUtils：时间格式化工具类
- ToastUtils：显示Toast的工具类

### Widget
- AutoCardView：配合AutoLayout的CardView
- ClearableEditText：带清空功能的编辑框
- DateAndTimePicker：时间和日期选择器
- ListViewForScrollView：适配ScrollView的ListView
- LoadAndRefreshView：上拉加载更多，下拉刷新控件
- NoScrollViewPager：不可以滑动的ViewPager
- RoundImageView：圆形ImageView

### 其他
库内已经集成Material Design一系列支持库，GSON基础库，另外还有[EventBus](https://github.com/greenrobot/EventBus)，[AutoLayout](https://github.com/hongyangAndroid/AndroidAutoLayout)，[TextSurface](https://github.com/elevenetc/TextSurface)，[LikeButton](https://github.com/jd-alexander/LikeButton)，[MPAndroidChart](https://github.com/PhilJay/MPAndroidChart)等一些优秀的库。

## 使用方法
将库下载下来，将cookie-library作为Module导入项目即可。因为使用了其他的库，可能会报错，这个时候需要在app的build.gradle里加上如下代码即可：

```
repositories {
    maven { url "https://jitpack.io" }
}
```

或者你可以去掉你不想使用的库。

## 下载地址
GitHub：[Cookie-Library](https://github.com/tsubasa-kun/Cookie-Library)

## 致谢
灵感来自：[顾哥](https://github.com/NateRobinson)

核心库：[xUtils3](https://github.com/wyouflf/xUtils3)