# Windows的cmd命令查询指定端口占用的进程并关闭

以端口8080为例：

1.查找对应的端口占用的进程：netstat  -aon|findstr  "8080"    ，找到占用8080端口对应的程序的PID号：

2.根据PID号找到对应的程序：tasklist|findstr "PID号"    ，找到对应的程序名

3.结束该进程：taskkill /f /t /im 程序名