# problem-sample

This is a project about the problem's format in TUOJ.

# 目录格式
	- doc // 在线文档，比赛/网页可见内容
	- files // 评测相关文件，不可见
	- data // 评测数据
	- etc
		- [conf]
		- [init]
	[- down] 下发文件

# 与服务器的交互

	在 server 上创建一个项目。之后你可以在 server 上手动要求 pull 操作。
	
	服务器

# conf
# sample
	- doc  // 在线文档，比赛/网页可见内容
		- description.md
	- core // 评测核心，所有的源代码
	- data // 数据
	- etc
		- [conf] // 题目配置，指导服务器如何使用这一道题
		- [init] // 指导服务器初始化的脚本
	[- down] 下发文件

# 评测
	评测时创建一个 docker，并到 docker 内。

# gitlab 题库与服务器的交互
	在 server 上创建一个项目。之后你可以在 server 上利用 pull 按钮来更新题目。
	在未来我们可能尝试添加一个钩子，使得 push 到 gitlab 后 server 会自动 pull（但我认为目前没有必要）
	
## conf 交互
	conf 是一个 json 文件，见 conf/readme.md。

## init 
	init 为服务器指示了当 pull 新的题目后，初始化环境时应该执行的内容。所遵循的规范见 init/readme.md。