# maven 换源

在 `setting.xml` 添加以下，更换为阿里源：

```xml
<mirrors>
  <mirror>
    <id>alimaven</id>
    <name>aliyun maven</name>
    <url>http://maven.aliyun.com/nexus/content/groups/public/</url>
    <mirrorOf>central</mirrorOf>        
  </mirror>
</mirrors>
```

根据本机情况配置文件在用户目录 `.m2` 文件夹下或 maven 安装目录下 `conf` 文件夹下。