# Stack换源

请直接参考：https://mirrors.tuna.tsinghua.edu.cn/help/stackage/

以下内容可能过时：

- 使用`config.yaml`文件进行配置。

  文件位置如下：

  - Windows：`‪C:\sr\config.yaml`
  - Linux & Mac OS：`~/.stack/config.yaml`

- [`config.yaml`](config.yaml)文件内容（使用[浙大源](http://mirrors.zju.edu.cn)）:

  ```
  # This file contains default non-project-specific settings for 'stack', used
  # in all projects.  For more information about stack's configuration, see
  # http://docs.haskellstack.org/en/stable/yaml_configuration/
  
  # The following parameters are used by "stack new" to automatically fill fields
  # in the cabal config. We recommend uncommenting them and filling them out if
  # you intend to use 'stack new'.
  # See https://docs.haskellstack.org/en/stable/yaml_configuration/#templates
  templates:
    params:
  #    author-name:
  #    author-email:
  #    copyright:
  #    github-username:
  
  package-indices:
  - name: ZJU
    download-prefix: https://mirrors.zju.edu.cn/hackage/package/
    http: https://mirrors.zju.edu.cn/hackage/00-index.tar.gz
  setup-info: "http://mirrors.zju.edu.cn/stackage/stack-setup.yaml"
  urls:
    latest-snapshot: http://mirrors.zju.edu.cn/stackage/snapshots.json
    lts-build-plans: http://mirrors.zju.edu.cn/stackage/lts-haskell/
    nightly-build-plans: http://mirrors.zju.edu.cn/stackage/stackage-nightly/
  ```

