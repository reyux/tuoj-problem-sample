# problem-sample

This is a project about the problem's format in TUOJ.

# 目录格式
	- doc // 在线文档，比赛/网页可见内容
	- files // 评测相关文件，不可见
	- data // 评测数据
	- etc
		- [conf]
		- [init]
		- [test]
	[- test] // 测试用文件
	[- down] 下发文件

# 与服务器的交互

	在 server 上创建一个项目。之后在 server 上手动要求 pull 操作。
	
	服务器与 git 同步的目录不做任何改变。应当在其他路径下另开一个目录 core 作为评测时的可用目录。
	
# etc/conf

# etc/init
	init 将指导服务器如何初始化 core 。应当可以设置为自动或者手动。
	
	init 文件中每行一句命令。
	
	提供的命令如下：
	
	- compile <file> [command] 根据后缀名编译文件 file，添加 command 参数。
	- mktest <start, end>		
	- make                     调用 files/make (如果文件存在)。服务器应当严格限制该命令。

# etc/test
	在 pull 操作后，可以利用 test 目录下的文件进行测试。
	也可以自己在线提交测试，这样提交的测试记录在服务器端。