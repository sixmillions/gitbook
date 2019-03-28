# 第三节:Docker相关命令

---
## 常用命令
- 查找镜像  
`docker search -s 3 nginx`  
- 拉取镜像  
`docker pull nginx`  

---
##Docker容器进入
- 使用docker attach进入Docker容器
`docker attach docker的id`  
> 该命令有一个问题。当多个窗口同时使用该命令进入该容器时，所有的窗口都会同步显示。如果有一个窗口阻塞了，那么其他窗口也无法再进行操作。  
**docker attach命令不太适合于生产环境，平时自己开发应用时可以使用该命令**

- 使用nsenter进入Docker容器  
[博客](https://www.cnblogs.com/xhyan/p/6593075.html)

---
### 给容器挂载存储卷
- `-v` 给容器挂载存储卷，挂载到容器的某个目录
- [其他docker run 参数](https://www.cnblogs.com/yfalcon/p/9044246.html)
> 例如  
`docker run --name gitbook1-nginx -v /sixmillions/test/_book:/usr/share/nginx/html -d -p 8010:80 nginx`  
这里面 -v就是把_book目录挂载到容器的html目录  
-p 是端口映射.这里访问4000,就是访问容器的80端口
-d 是后台运行  

---




