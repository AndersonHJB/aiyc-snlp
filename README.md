# 📦 Bornforthis Library Python aiyc1v1

## 1. What?

带编程一对一学员学习 Python 所开发的库，便于零基础小白学习。和部分实用功能，目前拥有：

- [x] 简单的 NLP

- [x] 类游戏
- [x] NoteSearch：[https://github.com/AndersonHJB/aiyc1v1/tree/main/aiyc1v1/NoteSearch](https://github.com/AndersonHJB/aiyc1v1/tree/main/aiyc1v1/NoteSearch)
- [x] 爬虫延迟插件「DelayWait」：[https://github.com/AndersonHJB/aiyc1v1/tree/main/aiyc1v1/DelayWait](https://github.com/AndersonHJB/aiyc1v1/tree/main/aiyc1v1/DelayWait)

如果，你有想要实现的功能，迟迟未实现，可以提交 issue 给我。[https://github.com/AndersonHJB/aiyc1v1/issues](https://github.com/AndersonHJB/aiyc1v1/issues)



## 2. Install

如果你换源了，请用下面的命令获取最新版本：

```python
pip install aiyc1v1 -i https://pypi.org/simple
```

国内镜像源同步，比较缓慢，一般需要一天左右才会同步。

```python
pip install aiy1v1
```

## 3. Upgrade

版本在快速的迭代中，所以如果需要最新版本的话，请用下面的命令。

```python
pip3 install --upgrade aiyc1v1 -i https://pypi.org/simple
```

```python
pip3 install --upgrade aiyc1v1
```



## 4. 项目文档

本部分是对已有的项目进行详细介绍，自行点入进行阅读。

- NoteSearch：[README](https://github.com/AndersonHJB/aiyc1v1/blob/main/aiyc1v1/NoteSearch/README.md)
- 爬虫延迟插件：



## 5. Github

本项目的 GitHub 地址：[https://github.com/AndersonHJB/aiyc1v1](https://github.com/AndersonHJB/aiyc1v1)



## 6. 已有功能代码

- [x] SimpleNLP:简单的自然语言处理代码「仅仅支持英文」——词频分析、词云生成。文档：[SimpleNLP.md](./docs/SimpleNLP.md)
- [x] GameBase:基础文字对话游戏
- [x] NoteSearch:[文档](./aiyc1v1/NoteSearch/README.md)
- [x] DelayWait: 智能爬虫插件「2023年01月07日」

## 7. 使用示例

### NoteSearch

```python
from aiyc1v1 import DataManger, Search_Engine

abs_path = "your/project/path"
d = DataManger(path=abs_path)

s = Search_Engine(language="zh_CN")
s.search("专栏")
```



### DelayWait

更智能的延迟请求插件，使你摆脱单纯使用 `time.sleep()`。具体实现逻辑，我也会在该插件文档中为你解答。

```python
from aiyc1v1 import DelayWait
import requests
if __name__ == '__main__':
    urls = ["https://bornforthis.cn"] * 10
    d = DelayWait()
    for url in urls:
        html = requests.get(url)
        d.wait(url)
        print(html.status_code)
```
## Error

### 2022年08月20日

```python
numpy.core._exceptions.UFuncTypeError: ufunc 'add' did not contain a loop with signature matching types (dtype('float64'), dtype('<U1')) -> None
```

预测是 dataframe to str 的错误，直接把读取到的结果，强制转换成 str

```python
self.content = str(pd.read_csv(self.path))
self.content = str(pd.read_excel(self.path))
```





## Changelog

- Bug Fixes：bug 修复
-  ⚠ BREAKING CHANGES：⚠ 重大变化
- Features：特征
- Reverts：还原
- Performance Improvements：性能改进

## 2023年01月12日

### Bug

- 文件读取，过程中，编码问题。

### Features

- 多语言支持
- 询问用户：查询到 xx 条数据，请问要返回几条？、全部「all」
- 



### 2023年01月06日

- [x] 正式发布可用的 NoteSearch
- [x] 初步解决编写代码，文档中搜索问题

### 2022年08月20日

1. 修改用户输入提示
```python
template = "您选择使用默认路径:%s, \n如果确认请输入回车或者 yes(否则:no):"
```
to
```python
template = "您选择使用路径:%s, \n如果确认请输入回车或者 yes(否则:no):"
```
## 公众号：AI悦创【二维码】

欢迎关注我公众号：AI悦创，有更多更好玩的等你发现！

![](https://bornforthis.cn/gzh.jpg)

## info AI悦创·编程一对一

AI悦创·推出辅导班啦，包括「Python 语言辅导班、C++ 辅导班、java 辅导班、算法/数据结构辅导班、少儿编程、pygame 游戏开发」，全部都是一对一教学：一对一辅导 + 一对一答疑 + 布置作业 + 项目实践等。当然，还有线下线上摄影课程、Photoshop、Premiere 一对一教学、QQ、微信在线，随时响应！微信：Jiabcdefh

C++ 信息奥赛题解，长期更新！长期招收一对一中小学信息奥赛集训，莆田、厦门地区有机会线下上门，其他地区线上。微信：Jiabcdefh

方法一：[QQ](http://wpa.qq.com/msgrd?v=3&uin=1432803776&site=qq&menu=yes)

方法二：微信：Jiabcdefh


![](https://bornforthis.cn/zsxq.jpg)

[![Security Status](https://www.murphysec.com/platform3/v3/badge/1610659414206361600.svg?t=1)](https://www.murphysec.com/accept?code=6e60439b6c9115849c8c231139adc3f5&type=1&from=2&t=2)