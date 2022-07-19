# npm 换源

- 临时使用

  ```shell
  $ npm --registry https://registry.npmmirror.com install xxx
  ```

- 换淘宝源

  ```shell
  $ npm config set registry https://registry.npmmirror.com
  ```

- cnpm

  - 通过安装

    ```shell
    $ npm install -g cnpm --registry=https://registry.npmmirror.com
    ```

  - 通过 alias

    ```
    alias cnpm="npm --registry=https://registry.npmmirror.com \
    --cache=$HOME/.npm/.cache/cnpm \
    --disturl=https://npmmirror.com/mirrors/node \
    --userconfig=$HOME/.cnpmrc"

    # Or alias it in .bashrc or .zshrc
    $ echo '\n#alias for cnpm\nalias cnpm="npm --registry=https://registry.npmmirror.com \
      --cache=$HOME/.npm/.cache/cnpm \
      --disturl=https://npmmirror.com/mirrors/node \
      --userconfig=$HOME/.cnpmrc"' >> ~/.zshrc && source ~/.zshrc
    ```

- More

  - 查看 npm 源地址

    ```shell
    $ npm config get registry
    ```

  - 换回官方镜像

    ```shell
    $ npm config set registry https://registry.npmjs.org/
    ```

淘宝镜像地址：https://registry.npmmirror.com
