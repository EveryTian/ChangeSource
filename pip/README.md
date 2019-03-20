# pip 换源

- 一次使用

  ```shell
  pip install -i https://mirrors.aliyun.com/pypi/simple xxx
  ```

- 换源

  编辑 [`pip.conf`](pip.conf) 文件如下：

  ```
  [global]
  index-url = https://mirrors.aliyun.com/pypi/simple/
  [install]
  trusted-host=mirrors.aliyun.com
  ```

  - Windows 下文件位置：`C:\Users\XXX\pip\pip.conf`
  - Linux & Mac OS 下文件位置：`~/.pip/pip.conf`

- 此外还有

  - TUNA 源：<https://pypi.tuna.tsinghua.edu.cn/simple>
  - 豆瓣源：[http://pypi.douban.com/simple/](https://pypi.douban.com/simple/) 

