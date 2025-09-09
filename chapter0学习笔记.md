linux基础指令：
导航与目录操作
命令	全称/含义	功能说明	示例
pwd	Print Working Directory	显示你当前所在的目录路径	pwd
ls	List	列出当前目录下的文件和文件夹	ls ls -l (详情) ls -a (显示隐藏文件)
cd	Change Directory	切换目录	cd /home (绝对路径) cd Documents (相对路径) cd .. (上一级) cd ~ 或 cd (回家目录)
mkdir	Make Directory	创建新目录	mkdir new_folder mkdir -p parent/child (创建多级目录)
rmdir	Remove Directory	删除空目录	rmdir empty_folder


文件操作
命令	全称/含义	功能说明	示例
touch	-	创建一个新的空文件或更新文件时间戳	touch new_file.txt
cp	Copy	复制文件或目录	cp file.txt copy.txt cp -r dir1/ dir2/ (复制目录)
mv	Move	移动文件/目录，或为其重命名	mv old.txt new.txt (重命名) mv file.txt ~/Documents/ (移动)
rm	Remove	删除文件或目录	rm file.txt rm -r folder/ (删除目录及内容) rm -f file (强制删除，无提示) 慎用！
cat	Catenate	查看文件全部内容（适合小文件）	cat file.txt
less / more	-	分页查看文件内容（适合大文件）	less long_file.log (按 q 退出)
head	-	查看文件开头几行（默认10行）	head file.log head -n 20 file.log (看前20行)
tail	-	查看文件末尾几行（默认10行）	tail file.log tail -f file.log (实时追踪日志更新)


系统信息与权限
命令	全称/含义	功能说明	示例
ps	Process Status	查看当前进程状态	ps ps aux (查看所有进程)
top / htop	-	动态显示、管理运行中的进程（任务管理器）	top (按 q 退出)
kill	-	终止进程	kill 1234 (终止PID为1234的进程) kill -9 1234 (强制终止)
chmod	Change Mode	修改文件或目录的权限	chmod +x script.sh (添加可执行权限)
sudo	Super User Do	以超级管理员（root）身份执行命令	sudo apt update
df	Disk Free	查看磁盘空间使用情况	df -h (以易读格式显示)
free	-	查看内存使用情况	free -h (以易读格式显示)


网络与帮助
命令	全称/含义	功能说明	示例
ping	-	测试与另一台网络的连通性	ping google.com (按 Ctrl+C 停止)
curl / wget	-	从网络下载文件或测试API	curl https://example.com wget https://example.com/file.zip
man	Manual	查看命令的详细帮助手册（最权威）	man ls (查看 ls 命令的用法，按 q 退出)
--help	-	快速查看命令的常用选项和帮助	ls --help




网络知识：

一、子网划分 (Subnetting):

通过借用IP地址的主机位来创建多个更小的逻辑网络（子网），从而将一个大的IP网络划分成多个小型网络.

为什么要划分子网？

1.提高网络性能：减少广播域范围，降低网络拥堵
2.增强安全性：在不同子网间实施访问控制策略
3.便于管理：按部门、功能或地理位置逻辑分隔网络
4.节省IP地址：更有效地分配IP地址资源

二、公网 vs. 局域网

公网是全球范围的开放网络，使用付费且唯一的公有IP；局域网是局部区域的私有网络，使用免费的私有IP并由组织独立控制，可以重复使用。

三、 两台服务器间网线直连配置

物理连接，使用普通网线（直通线）连接两台服务器的网口，现代网卡支持自动翻转功能，无需特殊交叉线，确认网口指示灯亮起表示物理连接正常

