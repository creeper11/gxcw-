# gxcw-
字段信息
•	.vscode:
•	这是一个隐藏目录，它包含了Visual Studio Code编辑器的配置文件，比如设置、代码片段、任务和调试配置等。
•	controller:
•	包含控制器（Controller）层的代码，控制器通常负责处理HTTP请求并将它们映射到业务逻辑。
•	docs:
•	这个目录可能包含项目的文档，比如API文档、开发指南或其他相关的文档资料。
•	middleware:
•	包含中间件（Middleware）代码，中间件是在请求处理过程中执行额外任务的函数，比如身份验证、日志记录、跨源资源共享（CORS）等。
•	model:
•	包含数据模型（Model）层的代码，通常与数据库交互，定义数据结构和业务逻辑。
•	router:
•	包含路由（Router）配置，它定义了URL路径和控制器之间的映射。
•	service:
•	包含服务（Service）层的代码，服务层通常封装业务逻辑，供控制器层调用。
•	source:
•	这个目录的用途可能比较特殊，但通常可以包含源代码文件，比如工具类、第三方库的封装或其他共享资源。

https://github.com/modood/Administrative-divisions-of-China?tab=readme-ov-file
可以用这个行政区域数据

https://g-wmpa2994.coding.net/p/gxcw/ci/job/5292215/build/104/pipeline
MongoDB
集合
users：移动端 用户的信息
username	用户名		string	类型
password	用户密码	string	类型
phone		手机号		string	类型
gender		性别		string	类型
age			年龄	 	int		类型
nationality    国籍			string 	类型
ethnicity  	民族		string  	类型
id_card		身份证号码	string	类型
address    	地址		string 	类型
created_at	注册时间	string	类型
token		验证		string	类型
employees：PC端 员工的信息
	employeeid		员工ID		string	类型
employeename	员工名		string	类型
password		用户密码	string	类型
phone			手机号		string	类型
gender			性别		string	类型
age				年龄	 	int		类型
created_at		注册时间	string	类型
token			验证		string	类型

Register的测试
{
    "employeeid":"10001",
    "employeename":"李芳",
    "password":"123456",
    "phone":"173123456789",
    "gender":"女",
    "age":22			
}

integrals：积分信息
name		用户名		string	类型
phone		手机号		string	类型
balance   	积分余额	int    	类型
created_at	注册时间	string	类型
updated_at	修改时间	string	类型


area 		区县级行政区域信息
    Code          string 		县级编码
    Name          string 		区县名称
    CityCode      string 		该区县对应地级市的名称
    Provincescode string 		该区县对应省份的名称

cities：	地级市行政区域信息
    
code          string 该市编码
    name          string 该市名称
    provincescode string 对应省份编码
province：	 省行政区域信息
code          string 该省编码
    name          string 该省名称

parkingspot ：车位信息
psid 			string	 车位id	
username           string		用户名（车位的所属者）
provincescode  string   	省编码
citycode       string 	市编码
areacode       string 	区县编码 
address			 string        	详细地址
status			 int      		车位状态 0 空位  1 出租

order：订单信息
orderid			string			订单id
psid 			string			车位id	
ordername 		string			客户
cost				double(float64)	金额
rent_bat			string			开始租车位
rent_eat			string			结束租车位


swag 安装
复制代码

$ go get -u github.com/swaggo/swag/cmd/swag

# 1.16 及以上版本
$ go install github.com/swaggo/swag/cmd/swag@latest
启动
swag init




