# 文章语法样例

## 代码块样例

```python title='demo.py'
def sayhi():
    return "hi,Python全栈开发"
```

## 提示框

`??? note "标题" `  三个问号表示提示框要折叠，`!!! success "标题" ` 三个叹号表示提示框不折叠，提示框中的内容要 **向内缩进一层** 。

有 11 种提示框

??? note "这是 note 类型的提示框"
    提示：更多精彩内容记得关注我啊

    注意，函数接收并返回的值是 3（ int），不是 "3"（str）。

    FastAPI 通过类型声明自动**解析**请求中的数据。


!!! note "这是 note 类型的提示框"
    提示：更多精彩内容记得关注我啊

    注意，函数接收并返回的值是 3（ int），不是 "3"（str）。

    FastAPI 通过类型声明自动**解析**请求中的数据。

!!! summary  "这是 summary 类型的提示框"
    summary

!!! info   "这是 info  类型的提示框"
    info 

!!! tip   "这是 tip  类型的提示框"
    tip 

!!! warning   "这是 warning  类型的提示框"
    warning 

!!! danger   "这是 danger  类型的提示框"
    danger 

!!! quote    "这是 quote   类型的提示框"
    quote  

!!! success "这是 success 类型的提示框"
    成功！

!!! failure "这是 failure 类型的提示框"
    失败！

!!! bug "这是 bug 类型的提示框"
    发现一个 bug，请尽快修复！

!!! question "question, help, faq"
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.






## 引用

在要插入引用的地方，使用 `[^1]` 来标记引用。

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

这里是正文。

最后统一编写引用 

```
[^1]: xxxxxx
[^2]: nnnnnn
```

## 代码并列显示效果

需要启用 `pymdownx.tabbed`  插件, 并且添加配置

```
- pymdownx.tabbed:
    alternate_style: true


```


=== "Python 3.10+"

    ```python
    from typing import Union
    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/items/{item_id}")
    async def read_item(item_id: str, q: Union[str, None] = None):
        if q:
            return {"item_id": item_id, "q": q}
        return {"item_id": item_id}
    ```

=== "Python 3.8+"

    ```python
    from typing import Union
    from fastapi import FastAPI

    app = FastAPI()

    @app.get("/items/{item_name}")
    async def read_item(item_name: str, q: Union[str, None] = None):
        if q:
            return {"item_id": item_name, "q": q}
        return {"item_id": item_name}
    ```




[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
[^2]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.