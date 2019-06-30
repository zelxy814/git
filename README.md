## .md(markdown)文件的基本语法
- Markdown 是一种轻量级标记语言
## 标题
#### 第一种 前面带 # h几即前面写几个 #
```
  # 一级标题   >  <h1>一级标题</h1>
  ## 二级标题
  ### 三级标题
  ......
  ####### 七级标题
```
#### 第二种 只能表示一级和二级标题，=和-的数量不限制，大于一个即可
```
  一级标题
  =========
  二级标题
  --------
```
## 列表
#### 无序列表
```
  * 1                       .1
  + 1            > 预览     .1
  - 1                       .1

  <ul>
  <li>1</li>
  <li>1</li>
  <li>1</li>
</ul>
```
#### 有序列表
```
1. 列表                            1. 列表     
2. 列表            > 预览          2. 列表
3. 列表                            3. 列表
！数字后面的点只能是英文点
！！有序列表的序号是根据第一行列表的数字顺序来的
<ol>
  <li>列表</li>
  <li>列表</li>
  <li>列表</li>
</ol>
```
## 引用
> 这是一段引用代码
## 分割线
```
  ***
  ---
```
---
## 链接
```
 ### 行内式
 [Windows/Mac/Linux 全平台客户端](https://www.zybuluo.com/cmd/)
 <p><a href="https://www.zybuluo.com/cmd/">Windows/Mac/Linux 全平台客户端</a></p>

###参数式
[Windows/Mac/Linux 全平台客户端](https://www.zybuluo.com/cmd/ 'title属性')
<p><a href="https://www.zybuluo.com/cmd/" title="title属性">Windows/Mac/Linux 全平台客户端</a></p>
```
## 图片
```
![cmd-markdown-logo](https://www.zybuluo.com/static/img/logo.png)
<p><img src="https://www.zybuluo.com/static/img/logo.png" alt="cmd-markdown-logo" title="" /></p>
```
## 代码段
`我是单行文本`
多行使用前后三个 ```
## 文本样式
```
*字体倾斜*                >        <em>字体倾斜</em>
_字体倾斜_
**字体加粗**              >        <strong>字体加粗</strong>
__字体加粗__
~~字体删除~~              >        <del>字体删除</del>

  ! 符号与字体之间不要有空格
```
## 表格
```
| 项目        | 价格    |  数量   |
| --------    | -----: | :----:  |
| 计算机      | \$1600  |   5    |
| 手机        |   \$12  |   12   |
| 管线        |    \$1  |   234  |

: 是对齐方向
```
| 项目        | 价格    |  数量   |
| --------    | -----: | :----:  |
| 计算机      | \$1600  |   5    |
| 手机        |   \$12  |   12   |
| 管线        |    \$1  |   234  |

: 是对齐方向
