# 常用的一些Linux命令
## 1.查看Linux的核数
cat /proc/cpuinfo查看系统整个的CPU信息\
sort 将文本内容加以排序\
uniq 用于检查和删除其中重复的行\
wc用于计算字数，其中wc -l用于计算行数

物理CPU的个数（实实在在能看到的cpu的个数）\
cat /proc/cpuinfo | grep 'processor' | sort | uniq | wc -l\
每块CPU上的核数\
cat /proc/cpuinfo | grep 'core id' | sort | uniq | wc -l\
逻辑CPU个数，一般为对应的总的CPU数两倍\
cat /proc/cpuinfo | grep 'processor' | sort | uniq | wc -l

## 2.物理系服务器
node 所有节点占据情况\
j (-a) (所有人)队列情况查看