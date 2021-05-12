# 培训计划（原生Android开发快速入门）

<!-- **本培训计划分为几部分** -->
## 本培训计划分为几部分

- 培训的对象
- 培训的内容
- 培训到什么程度
- 培训完毕后的成果物

下面我们一个一个说

## 培训的对象

- 具有Java基础（或kotlin基础）、没有Android基础的同事

## 培训到什么程度
### 让参加培训的同事：
- 掌握如何根据设计图绘制UI界面
- 掌握如何在Android APP里面发送网络请求，并解析返回的json数据
- 掌握如何绘制列表，并且动态的根据网络返回的数据更新列表内容
- 掌握如何给Android APP打包

## 培训的成果物
- 仿微信首页、朋友圈、我的三个页面、以及tab切换功能

## 培训的内容
### 内容的选取上，遵循二八原则，只讲最常用的20%的内容，覆盖80%的应用场景
#### Android开发环境搭建、当前流行的Android开发技术
- Android Studio 安装与配置
- Android SDK介绍与安装注意事项
- Android模拟器安装与开发配置（布局视图）
- 真机开发配置（开发者模式+USB调试）
- 新建Android项目
- 运行Android项目
- Android项目的目录结构
- Android Jetpack（Google官方提供的各种库的统称）
- support与androidx
- 学习开源代码的注意事项
- Android Material Design（Google官方提供的UI规范及UI库）
- Android依赖管理
- 实战：用第三方包快速完成banner功能

#### Android页面布局、常用UI控件
- Android Studio UI Editor的使用
- LinearLayout
- 实战案例：仿微信底部tab
- RelativeLayout
- GridLayout
- 实战案例：仿微信朋友圈的九张图片
- FrameLayout（后面详细讲）
- ConstraintLayout拖拽开发
- Material Design常用控件（TextView、ImageView、EditText）
- 如何查看别人的App：UIAutomatorViewer
- 实战案例：仿微信“我的”页面

#### Android最基础组件——Activity与Fragment
- Activity的介绍与使用（页面跳转）
- AndroidManifest的介绍
- 实战案例：页面跳转
- UI组件操作
- Fragment的介绍与使用（页面切换）
- 实战案例：使仿微信底部tab具有切换页面功能

#### Android的列表
- RecyclerView的介绍与使用
- 设计模式——适配器模式
- RecyclerView的Adapter与Holder
- 下拉刷新与上拉加载
- 实战案例：仿微信聊天列表
- 作业：仿微信朋友圈（静态页面）

#### Android网络请求与json解析
- Android常用的网络请求库 okhttp
- Android常用的json解析库 Gson
- okhttp+Gson封装与使用
- 实战案例：仿微信朋友圈（动态填充数据）

#### Android开发架构MVVM
- MVVM的介绍、与MVC、MVP的区别
- MVVM在Android中对应的具体组件
- ViewModel的介绍与使用
- Mutable的介绍与使用
- 实战案例：Android打包
