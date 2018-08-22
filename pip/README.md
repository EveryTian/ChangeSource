# pip 换源

- 一次使用

  ```shell
  pip install -i http://mirrors.aliyun.com/pypi/simple xxx
  ```

- 换源

  编辑[`pip.conf`](pip.conf)文件如下：

  ```
  [global]
  index-url = http://mirrors.aliyun.com/pypi/simple
  ```

  - Windows下文件位置：`C:\Users\XXX\pip\pip.conf`
  - Linux & Mac OS下文件位置：`~/.pip/pip.conf`

- 此外还有

  - TUNA源：<https://pypi.tuna.tsinghua.edu.cn/simple>
  - 豆瓣源：[http://pypi.douban.com/simple/](https://pypi.douban.com/simple/) 

