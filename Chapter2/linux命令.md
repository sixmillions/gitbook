# 第一节:linux命令

***
##Linux查看端口占用情况,并强制释放占用的端口

1. 查找被占用的端口
```
netstat -tln 
netstat -tln | grep 8080
```
> netstat -tln 查看端口使用情况，而netstat -tln | grep 8080则是只查看端口8080的使用情况

2. 查看端口属于哪个程序?或者被哪个进程占用
```
lsof -i:8080
```
> 如果提示: `-bash: lsof: command not found`
> 则需要安装一下lsof
> `yum install lsof -y`

3. 杀掉占用端口的进程  根据pid杀掉
```
kill -9 进程id 
```
> 进程id查询 `ps -ef | grep tomcat`





