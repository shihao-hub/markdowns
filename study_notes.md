# 2024/06/23

**1.** 今天学习了 XML 文件（菜鸟教程）

稍微总结一下，XML 和 JSON 一样都是存储数据的，只不过 XML 更详细一点，可以作为介于软件和硬件之间的另一种存储数据的方式，在持久化领域比 JSON 更好，因为它的信息更加详细，而且更适宜人阅读。

![image-20240623121324511](C:\Users\29580\Desktop\markdowns\Typora_study_notes\assets\image-20240623121324511.png)





# 2024/06/22 ...

> { Python }
>
> { PyQt5 }
>
> { MongoDB }
>
> { Redis }

**1.** ==目前学习和计划学习的内容：==

------

- Python 基础 + 进阶 + CookBook
- Python Django
- Python Flask
- Python 爬虫
- Python 网络编程

------

- MySQL + MongoDB + Redis

------

- PyQt5 快速开发与实战（电子书）

  > 试试吧，至今为止，这么多电子书我都学不进去。
  >
  > 就拿这本书试试吧，毕竟电子书和看官方文档是一个类型，如果电子书学不进去，只能学进
  >
  > 去纸质书的话，长久也是不行的。毕竟，很多技术官方文档才是最新最全最主要的！

------

- Vue.js

------

- 设计模式

------

- 数据结构
- 操作系统
- 计算机组成原理

------

```txt
# Redis 和 MongoDB 的适用场景

由于 Redis 的数据存储在内存中，因此它非常适合用作缓存和高速读写的应用场景。例如，我们可以使用 Redis 作为网站的页面缓存，将经常访问的页面存储在 Redis 中，以减小数据库的压力。此外，Redis 还可以用作消息队列、实时排行榜、分布式锁等功能。

而 MongoDB 适用于需要存储复杂结构的数据和灵活查询的场景。例如，我们可以使用 MongoDB 存储博客文章的内容和评论，其中文章可以是一个包含标题、内容和标签等字段的文档。当需要查询某个标签下的文章时，可以方便地使用 MongoDB 的查询语法进行查询。

# Redis 与 MongoDB 的协同使用

虽然 Redis 和 MongoDB 在某些方面有一定的重叠，但它们也有自己的优势和适用场景。在实际项目中，有时候可以考虑同时使用 Redis 和 MongoDB，以充分利用它们的优点。

举个例子，假设我们正在开发一个电子商务网站，需要实现商品的库存管理和限时促销功能。我们可以使用 MongoDB 存储商品的详细信息，例如名称、描述和价格等。而库存信息和促销信息可以使用 Redis 存储，因为这些数据需要经常进行读写操作，并且需要快速响应。

另外一个例子是在微服务架构中使用 Redis 和 MongoDB。我们可以使用 MongoDB 存储微服务之间共享的核心数据，而使用 Redis 存储短期的缓存数据和会话信息。这样可以充分利用 Redis 的高速读写能力和丰富的数据结构，来提升系统的性能和可扩展性。
```



**2.** 找到个好网站：[极客教程](https://geek-docs.com)，而且暂时总结了一点，那就是 Python 我看再多的书，还是需要实战才行，我说的实战是关于那些库函数的使用，用到的时候去弄懂，这样日积月累才能彻彻底底地掌握 Python。

**3.** Bootstrap 值得一学，CSS 框架入门。

## Python 库

### PyQt5

> Qt5

[手把手教你学习 PyQT5](https://blog.csdn.net/weixin_42475060/article/details/130327901)

今日总结一下：

目前我的体会是 Qt5 的主要难点是设计，前端展示怎么好看又方便才是主要的！

能找到个模板最佳，直接套模板实现功能即可。后端不需要太过于在意前端，毕竟前端是需要点美学功底的。能做出来还凑活的界面就够了。其他的交给专业的来。

**Q:  为什么不用浏览器的前端呢？那个明显更好看，交互的时候直接启动本地端口不就行了。不联网使用的产品，用 HTTP 协议又不是不行。**

3-6-2、QTextEdit综合案例



> **《PyQt5 快速开发与实战》**



#### 第六章 PyQt5 布局管理



### matplotlib

>

```python
# 1.导入相关库
import matplotlib as mpl
import matplotlib.pyplot as plt

# 2.创建figure画布对象
figure = plt.figure()
# 3.获取对应位置的axes坐标系对象
axes1 = figure.add_subplot(2, 1, 1)
axes2 = figure.add_subplot(2, 1, 2)
# 4.调用axes对象，进行对应位置的图形绘制
axes1.plot([1, 3, 5, 7], [4, 9, 6, 8])
axes2.plot([1, 2, 4, 5], [8, 4, 6, 2])
# 5.显示图形
figure.show()

# Result: png
```



### tqdm

> Python 的进度条库，可以在 Python 的循环中添加一个进度条，以便在终端中实时显示进度。

[Python主流处理PDF的库总结对比（包含详细示例）](https://blog.csdn.net/August_YdF/article/details/139836962)

<table><thead><tr><th> 库名 </th><th> 主要用途 </th><th style="width:212px;"> 主要功能 </th><th style="width:275px;"> 安装命令 </th></tr></thead><tbody><tr><td><strong>PyPDF2</strong></td><td> 操作和合并 PDF</td><td style="width:212px;"> 拆分、合并、旋转、裁剪 PDF 页面 &#xff0c; 提取文本和元数据 </td><td style="width:275px;"><code>pip install PyPDF2</code></td></tr><tr><td><strong>pdfminer.six</strong></td><td> 提取 PDF 文本 </td><td style="width:212px;"> 高精度提取文本、图像和表格 &#xff0c; 支持复杂布局和字体 </td><td style="width:275px;"><code>pip install pdfminer.six</code></td></tr><tr><td><strong>ReportLab</strong></td><td> 生成 PDF 文件 </td><td style="width:212px;"> 创建包含文本、图像、图形和表格的复杂 PDF 文档 </td><td style="width:275px;"><code>pip install reportlab</code></td></tr><tr><td><strong>PyMuPDF</strong></td><td> 读取和操作 PDF</td><td style="width:212px;"> 提取文本和图像 &#xff0c; 处理页面、注释和书签 &#xff0c; 渲染 PDF 页面 </td><td style="width:275px;"><code>pip install PyMuPDF</code></td></tr><tr><td><strong>pdfplumber</strong></td><td> 提取表格和文本 </td><td style="width:212px;"> 高精度提取和分析 PDF 中的表格和文本 </td><td style="width:275px;"><code>pip install pdfplumber</code></td></tr><tr><td><strong>Camelot</strong></td><td> 提取 PDF 表格 </td><td style="width:212px;"> 高精度表格检测和提取 &#xff0c; 导出为 CSV、Excel、JSON 等格式 </td><td style="width:275px;"><code>pip install camelot-py [cv]</code></td></tr><tr><td><strong>tabula-py</strong></td><td> 提取 PDF 表格 </td><td style="width:212px;"> 基于 Java 库 tabula&#xff0c; 提取表格为 DataFrame 或 CSV</td><td style="width:275px;"><code>pip install tabula-py</code></td></tr><tr><td><strong>Slate</strong></td><td> 提取 PDF 文本 </td><td style="width:212px;"> 基于 pdfminer 的简单文本提取工具 </td><td style="width:275px;"><code>pip install slate</code></td></tr><tr><td><strong>pdfquery</strong></td><td> 高级文本提取 </td><td style="width:212px;"> 结合 PDFMiner 和 lxml&#xff0c; 支持复杂查询和文本提取 </td><td style="width:275px;"><code>pip install pdfquery</code></td></tr><tr><td><strong>PDFKit</strong></td><td>HTML 转 PDF</td><td style="width:212px;"> 将 HTML 文档转换为 PDF&#xff0c; 基于 wkhtmltopdf 工具 </td><td style="width:275px;"><code>pip install pdfkit</code></td></tr><tr><td><strong>pdf2image</strong></td><td>PDF 转图像 </td><td style="width:212px;"> 使用 poppler 将 PDF 页面转换为 PIL 图像对象 </td><td style="width:275px;"><code>pip install pdf2image</code></td></tr></tbody></table>

### PyPDF2

>PyPDF2 是一个免费的、开源的纯 Python PDF 库，能够拆分、合并、裁剪和转换 PDF 文件的页面。它还可以为 PDF 文件添加自定义数据、查看选项和密码。 PyPDF2 也可以从 pdf 中检索文本和元数据。

[掌握 PDF 文件处理的神器：Python PyPDF2 库详解](https://www.51cto.com/article/790380.html)

[Python 使用 PyPDF2 库进行 PDF 文件操作的详细教程](https://cloud.tencent.com/developer/article/2383481)

```txt
# 安装 PyPDF2

# 基本 PDF 操作
## 1. 合并 PDF 文件
## 2. 分割 PDF 文件
## 3. 旋转 PDF 页面
## 4. 提取 PDF 文本

# 高级 PDF 操作
## 1. 添加水印
## 2. 加密 PDF 文件
## 3. 提取图像

# 总结
PyPDF2 是一个功能丰富的 Python 库，用于处理 PDF 文件。无论是需要合并、分割、旋转、提取文本，还是进行更高级的操作如添加水印、加密、提取图像，PyPDF2 都能满足需求。

通过本文的介绍和示例代码，可以更好地掌握 PyPDF2，将其应用于各种 PDF 文件处理任务中，提高工作效率，简化操作。
```

注意，PyPDF2 的功能较为基础，替换文本的功能是没有的，需要使用 PyMuPDF、pdfminer.six 等的绘图功能。

### PyMuPDF

> MuPDF
>
> 但是我发现了，它的不同版本，变化很大，查资料的时候乱七八糟的，api 都对不上，学习成本有点高。好无语，不兼容以前的吗？哪有你这样写代码的。

[Python 处理 PDF](https://blog.csdn.net/ling620/article/details/120035699)（这个挺好的）

[好家伙！神器啊！Python 处理 PDF —— PyMuPDF 的安装与使用！](https://cloud.tencent.com/developer/article/2104045)（和上面这个好像是同一个）

![image-20240622134620011](C:\Users\29580\Desktop\markdowns\Typora_study_notes\assets\image-20240622134620011.png)

```txt
直接将整个类发给 gpt3.5，问题：帮忙解析一下，我刚刚发给你的内容中，公共函数的含义。
下面是它的解析内容（不得不说，如果能够熟练使用 gpt，对个人能力的提升是巨大的）

在您提供的内容中，Page 类定义了多个公共函数和方法，以下是一些主要的：

__init__: 构造函数，用于初始化页面对象。
add_link: 添加一个新的链接到页面。
add_annot: 添加一个新的注释到页面。
add_widget: 添加一个新的表单控件到页面。
annot_xrefs: 获取页面中所有注释的 xref 列表。
annotations: 获取页面中的所有注释。
delete_link: 删除页面中的一个链接。
delete_annot: 删除页面中的一个注释。
draw_image: 在页面上绘制图像。
draw_rect: 在页面上绘制矩形。
draw_line: 在页面上绘制线条。
draw_circle: 在页面上绘制圆形。
draw椭圆形: 在页面上绘制椭圆形。
draw_polygon: 在页面上绘制多边形。
draw_path: 在页面上绘制路径。
draw_text: 在页面上绘制文本。
draw_link: 在页面上绘制链接。
draw_annot: 在页面上绘制注释。
draw_widget: 在页面上绘制表单控件。
extract_text: 从页面中提取文本。
get_images: 获取页面中定义的所有图像。
get_oc_items: 获取页面中使用的 OCGs 和 OCMDs。
get_textbox: 从页面中提取文本框的文本。
get_textpage: 获取页面的文本页对象。
get_xobjects: 获取页面中定义的所有 xobjects。
insert_font: 向页面中插入字体。
links: 生成页面中的所有链接。
load_annot: 加载页面中的注释。
load_links: 加载页面中的第一个链接。
load_widget: 加载页面中的表单控件。
mediabox: 页面的 MediaBox。
rotation: 页面的旋转角度。
rotation_matrix: 页面的旋转矩阵。
set_artbox: 设置页面的 ArtBox。
set_bleedbox: 设置页面的 BleedBox。
set_cropbox: 设置页面的 CropBox。
set_language: 设置页面的默认语言。
set_mediabox: 设置页面的 MediaBox。
set_rotation: 设置页面的旋转角度。
set_trimbox: 设置页面的 TrimBox。
widgets: 生成页面中的所有表单控件。
wrap_contents: 确保页面处于平衡的图形状态。
xref: 页面的 PDF xref 编号。
此外，还有一些静态方法和私有方法，以及一些属性定义，例如 rect、language、transformation_matrix 等。

请注意，这个列表可能不全面，因为代码中可能还包含其他方法和属性。
```









# 2024/06/17

> { docker }

**1.** 似乎安装 docker 的时候，会安装一部分 WSL（Windows SubSystem for Linux），并没有安装 Ubuntu，但是我执行 bash.exe 的时候，会去找 Linux 的目录。我将 bash.exe 改为 bash2.exe，使用 bash2 就解决了这个问题。但是使人疑惑的一点是：为什么就 bash 会这样呢？因为我发现在 cmd 中使用 ls，压根就找不到这个命令。那我用 bash 为什么会根据  Linux 目录搜索命令呢？Docker 桌面版干的好事？



# 2024/06/16

> { Bootstrap }
>
> { bat }

**1.** 需要使用 HTML5 文档类型（Doctype）因此，请在使用 Bootstrap 项目的开头包含下面的代码段。

```html
<!DOCTYPE html>
<html>
....
</html>
```

如果在 Bootstrap 创建的网页开头不使用 HTML5 的文档类型（Doctype），您可能会面临一些浏览器显示不一致的问题，甚至可能面临一些特定情境下的不一致，以致于您的代码不能通过 W3C 标准的验证。

**2.** 使用 Python 的正则表达式进行字符串替换的时候，突然意识到，这正则表达式是用 C 语言实现的，C 语言处理字符串的性能很高。所以根本不需要担心性能问题！（所以这是不是意味着，C 语言有机会也需要精通？但是感觉语言这东西，学是不可能完全精通的，只有可能精通一部分，而那部分是用到的时候好好学学，然后精通...）

**3.** Bootstrap 概览

```text
Bootstrap css

value attr tag_name
viewport name meta
img-responsive class img
container class div



```

**4.** 学 bat 的时候发现，问 gpt 能回答不少不需要我搜索的内容，挺省事的。







# 2024/06/15

> { Restful  }

**1.** Restful 关键的一句话是：将一切视为资源！

```txt
GET /posts
GET /posts/{post_id}
POST /posts
PUT /posts/{post_id}
DELETE /posts/{post_id}

POST /posts/actions/move
POST /posts/actions/distribute
```

**2.** 今天简单阅读源码的时候发现一个问题，使用 *args, **kwargs 的时候，最初的那个函数，大部分都是要写得明明白白的。

```txt
举个例子：
requests.get(...)
request('get', url, params=params, **kwargs)
session.request(method=method, url=url, **kwargs)

def request(self, method, url,
	params=None, data=None, headers=None, cookies=None, files=None,
	auth=None, timeout=None, allow_redirects=True, proxies=None,
	hooks=None, stream=None, verify=None, cert=None, json=None):
```

**3.** 到底如何组织代码呀！很有强迫症。或者说，到底怎么才能拥有那种把代码组织好的能力？目前看来这个工作是没有这个机会了。那只能自学，所以如何自学呢？有什么非常有价值学习的项目吗？

​	

**4.** 关于小鲁班

```python
"""
我想要实现一个类似如下功能的程序：
发生消息，它返回一个菜单
我在发送个数字，表示对应菜单的某个功能
然后接下来的对话就是基于这个功能的对话
"""

"""
要实现您描述的功能，您可以考虑以下步骤和思路：

1. 设计消息处理流程：
接收消息：程序接收用户发送的消息。
返回菜单：根据用户消息，返回相应的菜单，让用户选择功能。
2. 实现菜单选择功能：
用户选择：用户发送数字选择菜单中的功能。
处理选择：根据用户选择的数字，确定后续对话的功能。
3. 实现功能对话：
根据选择：根据用户选择的功能，展开相应的对话。
交互对话：与用户进行基于该功能的对话交互。
4. 示例代码框架：
您可以使用编程语言（如Python）和相关库（如Flask）来实现这个功能。以下是一个简单的示例代码框架：
"""

from flask import Flask, request, jsonify

app = Flask(__name__)

def process_message(message):
    # 根据消息处理逻辑，返回菜单
    menu = "1. 功能A\n2. 功能B\n3. 功能C"
    return menu

def process_choice(choice):
    # 根据用户选择处理逻辑
    if choice == '1':
        return "您选择了功能A，请输入相关信息"
    elif choice == '2':
        return "您选择了功能B，请输入相关信息"
    elif choice == '3':
        return "您选择了功能C，请输入相关信息"
    else:
        return "无效选择，请重新选择"

@app.route('/', methods=['POST'])
def handle_message():
    data = request.get_json()
    message = data['message']
    
    if message.isdigit():
        response = process_choice(message)
    else:
        response = process_message(message)
    
    return jsonify({"response": response})

if __name__ == '__main__':
    app.run()
```

**5.** 《流畅的 Python》这本书中通过协程模拟了一个仿真程序， 可以通过它了解一下仿真程序的部分基本原理。
