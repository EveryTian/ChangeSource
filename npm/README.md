# npm 换源

- 临时使用

  ```shell
  $ npm --registry https://registry.npm.taobao.org install xxx
  ```

- 换淘宝源

  ```shell
  $ npm config set registry https://registry.npm.taobao.org
  ```

- cnpm

  - 通过安装

    ```shell
    $ npm install -g cnpm --registry=https://registry.npm.taobao.org
    ```

  - 通过 alias

    ```
    alias cnpm="npm --registry=https://registry.npm.taobao.org \
    --cache=$HOME/.npm/.cache/cnpm \
    --disturl=https://npm.taobao.org/dist \
    --userconfig=$HOME/.cnpmrc"
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

淘宝镜像地址：[https://npm.taobao.org/](https://npm.taobao.org/)
