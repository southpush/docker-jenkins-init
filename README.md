# jenkins docker 初始化demo

sources.list 将apt源替换为阿里云源

plugins.txt 是jenkins要安装的插件列表，可以按自己的需求进行更改

构建：
```
docker built --tag <name>:<tag> .
```

使用：
```
docker run -d -p 8080:8080 -p 50000:5000 -v /var/run/docker.sock:/var/run/docker.sock <name>:<tag>
```

windows下绑定挂载docker套接字使用：
```
docker run -d -p 8080:8080 -p 50000:5000 -v //var/run/docker.sock:/var/run/docker.sock <name>:<tag>
```