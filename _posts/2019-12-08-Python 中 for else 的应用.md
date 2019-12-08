---
layout:     post
title:      Python 中 for else 的应用
subtitle:   
date:       2019-12-08
author:     阳光1990
header-img: 
catalog: true
tags:
    - Python
---

Python 中提供了 `for else` 循环，这里用一个示例介绍如何使用这个循环。

## 示例代码

```python

# 定义一个学生信息列表
students = [
    {"姓名" : "张三", "性别" : "男"},
    {"姓名" : "杨画", "性别" : "女"},
    {"姓名" : "李明", "性别" : "男"}
]

# 需要查找的学生
search = "王五"

for student in students:

    # 查找学生，如果找到退出循环
    if student["姓名"] == search:
        print("学生 %s 已经找到。" % search)
        break
else:
    # 循环到最后，未找到学生，输出提示信息。
    print("对不起：学生 %s 未找到。" % search)

print("查找结束！")

```

## 示例测试：

（1）查找的学生在列表中**存在**，如 `search = "杨画"`：

```
学生 杨画 已经找到。
查找结束！
```

（2）查找的学生在列表中**不存在**，如 `search = "王五"`：
```
对不起：学生 王五 未找到。
查找结束！
```
