# Markdown 语法介绍
----
## 标题
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
----
## 引用 >
> 这是第一级引用。
>
> > 这是第二级引用。
>
> 现在回到第一级引用。
----
## 列表
列表项目标记通常放在最左边，项目标记后面要接一个字符的空格。

#### 无序列表：使用星号、加号或是减号作为列表标记
- Red
- Green
- Blue

#### 有序列表：使用数字接着一个英文句点
1. Red
2. Green
3. Blue

#### 代办列表: 表示列表是否勾选状态（注意：[ ] 前后都要有空格）
- [ ] 不勾选
- [x] 勾选

#### 在列表项目内放进引用，那『>』就需要缩进：
*  Coding.net有以下主要功能:
    > 代码托管平台
    > 在线运行环境    
    > 代码质量监控    
    > 项目管理平台
    
## 代码
只要把你的代码块包裹在 “` 之间，你就不需要通过无休止的缩进来标记代码块了。 在围栏式代码块中，你可以指定一个可选的语言标识符，然后我们就可以为它启用语法着色了。 举个例子，这样可以为一段 Ruby 代码着色：
```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```
## 强调
在Markdown中，可以使用 * 和  _  来表示斜体和加粗。
#### 斜体：
*Coding，让开发更简单*
_Coding，让开发更简单_
#### 加粗：
**Coding，让开发更简单**
__Coding，让开发更简单__
#### 自动链接
方括号显示说明，圆括号内显示网址， Markdown 会自动把它转成链接，例如：
[超强大的云开发平台Coding](http://coding.net)

## 表格
在 Markdown 中，可以制作表格，例如：
First Header | Second Header | Third Header
------------ | ------------- | ------------
Content Cell | Content Cell  | Content Cell
Content Cell | Content Cell  | Content Cell

或者也可以让表格两边内容对齐，中间内容居中，例如：
First Header | Second Header | Third Header
:----------- | :-----------: | -----------:
Left         | Center        | Right
Left         | Center        | Right

## 分割线
在 Markdown 中，可以使用 3 个以上『-』符号制作分割线，例如：
这是分隔线上部分内容
---
这是分隔线上部分内容

## 图片
Markdown 使用了类似链接的语法来插入图片, 包含两种形式: 内联 和 引用.

内联图片语法如下:
![Alt text](/path/to/img.jpg)
或
![Alt text](/path/to/img.jpg "Optional title")

也就是:
一个惊叹号『!』
接着一个方括号，里面是图片的替代文字
接着一个普通括号，里面是图片的网址，最后还可以用引号包住并加上 选择性的『title’』文字。
引用图片语法如下:

![Alt text][id]
『id』 是图片引用的名称. 图片引用使用链接定义的相同语法:
[id]: url/to/image "Optional title attribute"

## 流程图
Markdown 编辑器已支持绘制流程图、时序图和甘特图。通过 mermaid 实现图形的插入，点击查看 更多语法详情。
```graph
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->E;
    E-->F;
    D-->F;
    F-->G;
```

## 时序图
```graph
sequenceDiagram
    participant Alice
    participant Bob
    Alice->John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts 
prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
```
