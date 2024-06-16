> 2024/06/16
>
> Bootstrap 1
>
> C 2

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









> 2024/06/15
>
> Python *

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
