# simple-douyin

极简版抖音,网络部分调用Gin框架，数据库用Gorm进行操作。数据库使用MySQL。nosql使用redis。外部依赖使用ffmpeg程序在视频上传时生成封面，并调用了github.com/u2takey/ffmpeg-go 库，可以在 go 语言端使用 ffmpeg 命令行工具。运用jwt-go生成、验证和保护客户端token。


## 项目结构
```
simple-douyin
├─ cache -redis缓存
│
├─ config -运行环境配置
│  
├─ handlers -解析路由请求参数         
│  
├─ lib - ffmpeg工具
│ 
├─ middleware -拦截器处理：jwt鉴权，密码加密等
│  
├─ models - 操作数据库
│  
├─ router - 路由
│  
├─ service -业务层处理相关参数调用
│  
├─ static - 视频与预览图片存放   
|        
└─ util -工具函数，包括视频处理工具等
  

```

## 运行

更改配置目录下对应信息
- mysql：相关配置
- redis：相关配置
- server ：服务器配置，用于生成视频与图片链接
- path ：ffmpeg文件路径
- conf.go ：解析文件config.toml的绝对路径

```
cd .\simple-douyin\
go run main.go
```
