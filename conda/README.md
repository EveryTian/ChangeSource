# conda 换源

- 使用以下三条指令

  ```shell
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
  conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
  conda config --set show_channel_urls yes
  ```

- 通过 `conda info` 进行状态的查看

  以本人结果为例：

  - 三条指令运行前

    ```
    C:\Users\EveryTian>conda info
    
         active environment : None
           user config file : C:\Users\EveryTian\.condarc
     populated config files :
              conda version : 4.5.8
        conda-build version : not installed
             python version : 3.6.6.final.0
           base environment : D:\Anaconda3  (writable)
               channel URLs : https://repo.anaconda.com/pkgs/main/win-64
                              https://repo.anaconda.com/pkgs/main/noarch
                              https://repo.anaconda.com/pkgs/free/win-64
                              https://repo.anaconda.com/pkgs/free/noarch
                              https://repo.anaconda.com/pkgs/r/win-64
                              https://repo.anaconda.com/pkgs/r/noarch
                              https://repo.anaconda.com/pkgs/pro/win-64
                              https://repo.anaconda.com/pkgs/pro/noarch
                              https://repo.anaconda.com/pkgs/msys2/win-64
                              https://repo.anaconda.com/pkgs/msys2/noarch
              package cache : D:\Anaconda3\pkgs
                              C:\Users\EveryTian\AppData\Local\conda\conda\pkgs
           envs directories : D:\Anaconda3\envs
                              C:\Users\EveryTian\AppData\Local\conda\conda\envs
                              C:\Users\EveryTian\.conda\envs
                   platform : win-64
                 user-agent : conda/4.5.8 requests/2.19.1 CPython/3.6.6 Windows/10 Windows/10.0.17134
              administrator : False
                 netrc file : None
               offline mode : False
    ```

  - 三条指令运行后

    ```
    C:\Users\EveryTian>conda info
    
         active environment : None
           user config file : C:\Users\EveryTian\.condarc
     populated config files : C:\Users\EveryTian\.condarc
              conda version : 4.5.8
        conda-build version : not installed
             python version : 3.6.6.final.0
           base environment : D:\Anaconda3  (writable)
               channel URLs : https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/win-64
                              https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/noarch
                              https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/win-64
                              https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/noarch
                              https://repo.anaconda.com/pkgs/main/win-64
                              https://repo.anaconda.com/pkgs/main/noarch
                              https://repo.anaconda.com/pkgs/free/win-64
                              https://repo.anaconda.com/pkgs/free/noarch
                              https://repo.anaconda.com/pkgs/r/win-64
                              https://repo.anaconda.com/pkgs/r/noarch
                              https://repo.anaconda.com/pkgs/pro/win-64
                              https://repo.anaconda.com/pkgs/pro/noarch
                              https://repo.anaconda.com/pkgs/msys2/win-64
                              https://repo.anaconda.com/pkgs/msys2/noarch
              package cache : D:\Anaconda3\pkgs
                              C:\Users\EveryTian\AppData\Local\conda\conda\pkgs
           envs directories : D:\Anaconda3\envs
                              C:\Users\EveryTian\AppData\Local\conda\conda\envs
                              C:\Users\EveryTian\.conda\envs
                   platform : win-64
                 user-agent : conda/4.5.8 requests/2.19.1 CPython/3.6.6 Windows/10 Windows/10.0.17134
              administrator : False
                 netrc file : None
               offline mode : False
    ```

    Channel URLs中多出TUNA源：

    ```
    https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/win-64
    https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/noarch
    https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/win-64
    https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/noarch
    ```

  运行后于家目录下（`~`或`C:\Users\XXX`）会生成[`.condarc`](.condarc)文件，其内容如下：

  ```
  channels:
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
    - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
    - defaults
  ```

- Conda 三方源

  - Conda Forge

    ```shell
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
    ```

  - msys2

    ```shell
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/
    ```

  - bioconda

    ```shell
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/bioconda/
    ```

  - menpo

    ```shell
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/menpo/
    ```

  - pytorch

    ```shell
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/pytorch/
    
    # for legacy win-64
    conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/peterjc123/
    ```

Anaconda 镜像站使用帮助：[https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)
