# gem换源

使用 [Ruby-China](https://gems.ruby-china.com/) 镜像：

RubyGems 版本建议 2.6.x 以上。 

> ```
> $ gem sources --add https://gems.ruby-china.com/ --remove https://rubygems.org/
> $ gem sources -l
> https://gems.ruby-china.com
> # 确保只有 gems.ruby-china.com
> ```
>
> 如果你使用 Gemfile 和 Bundler (例如：Rails 项目)
>
> 你可以用 Bundler 的 [Gem 源代码镜像命令](http://bundler.io/v1.5/bundle_config.html#gem-source-mirrors)。
>
> ```
> $ bundle config mirror.https://rubygems.org https://gems.ruby-china.com
> ```
>
> 这样你不用改你的 Gemfile 的 source。
