# Column、Row深入
## 主轴与交叉轴的概念及使用
- 主轴：主要的延伸方向
- 交叉轴：与主轴垂直的方向

# Expanded深入
- 一个时：占满剩余空间
- 多个时：按比例分配剩余空间

# Dart语法
- 访问控制：通过 _ 来控制访问权限

# Flutter的两种Widget
- StatefulWidget：有 状态
- StatelessWidget：less 反义 -> 没有 状态

状态：变量

## 新建Widget时，如何在上面两种中做选择
- 看有没有可变变量（没有final修饰），如果有就是StatefulWidget，如果没有就是StatelessWidget
- 如果是StatelessWidget，只需要写一个就行
- 如果是StatefulWidget，除了写Widget之外，还需要写一个State

咱项目基于waff开发，所有的Widget都用StatelessWidget
那变量放哪？-> 放到其他文件单独管理

# Material Design
## 主题：
- 参考url：
- 颜色：
## 布局：
- 参考url：
## 文字：
- 参考url：

# Figma与Material Design
- Figma中，对样式的属性，默认表示方式就是Material Design

## Figma样式中对Material Design的使用
- 边距：页面中，左右边距都是16
- 颜色：有主题色
- 字体：所有的文字都用了统一的字体

# Flutter中文字的单位
- 不需要写单位，它会根据各具体的平台把单位加上

# Flutter对Material Design是如何实现
## 开启Material Design支持
- pubspec.yml中：uses-material-design: true（为了可以使用Material Icon）
- 使用MaterialApp

## MaterialApp中的元素组成：
- appbar
- body

## Theme：定义全局样式
- 

### TextTheme
- 

# UI Widget
- Button

# Button
## 三种样式
- 实心
- 空心
- 文字
