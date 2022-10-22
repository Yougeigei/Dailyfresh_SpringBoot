# DailyFresh(天天生鲜Java Springboot电商项目)
天天生鲜是Python中Django框架的一个经典案例，现将其用java的SSM框架实现
包含了数据库文件，本项目需要用到redis存储用户浏览记录和购物车
这个项目当个课程大作业没问题。
## 版本信息

### 完成注册功能  
**实现功能：**
- 用户注册：前台校验，成功后发送ajax请求，控制器响应并向数据库表中添加数据
- 用户激活：通过产生唯一激活码查询用户并修改用户激活状态

### v1.2 完成登录功能
**实现功能：**
- 用户登录：通过用户名和密码查询用户并判断用户是否激活，登录成功后将用户存储在session中
- 退出登录：将存储在session中的用户信息清除
- 记住用户名：判断用户是否勾选`记住用户名`，将信息存在cookie中
- 主页顶部显示用户欢迎信息：通过判断session中是否有用户来显示欢迎信息
- **解决json解析问题**
- **500及以上的服务器异常会显示`error.jsp`页面，异常信息通过控制台输出**


### v1.3 用户中心
**实现功能：**
- 用户个人信息页面：查询用户基本信息显示在页面上
- 用户地址页面：查询用户默认收获地址显示在页面上
- 添加地址：向用户表对应的地址表中添加地址
- 拦截器：用户需要登录才能访问用户中心页面，设置一个跳转参数，用户登录后可直接跳转到被拦截的页面
- 页面抽取：将信息页面(error.jsp,registerOK.jsp,active.jsp)合并为一个(info.jsp)


### v1.4 后台管理(用户及其地址)
**实现功能：**
- 用户信息CRUD：查询所有用户并分页显示；增加用户；修改用户信息；删除用户(删除所有选中的用户)
- 地址信息CRUD：通过用户ID查询其地址显示；增加地址；修改地址；删除记录


### v1.5 后台管理基本完成
**实现功能：**
- 商品类型查询与修改：商品类型为固定内容，只能修改其图片url
- 商品SPU查询
- 商品SKU查询与修改
- 首页轮播图的CRUD
- 管理员首页
- **管理员登录**：包含验证码的校验
- **管理页面拦截器**


### v1.6 商品页面
**实现功能：**
- 首页：通过查询数据库显示内容
- 购物车数量：redis数据库存储用户购物车信息，可查询其商品种类数目进行显示
- 商品详情页面
- 商品列表页面
- 商品查询：通过模糊查询显示查询到的商品
- 商品添加购物车：购物车控制器响应


### v1.7 购物车
**实现功能：**
- 用户购物车页面(该页面被登录拦截器拦截)
- 商品选中动态修改商品总价和共计商品
- 购物车页面的增加减少和删除对应购物车控制器中的响应


### Ultimate
**实现功能：**
- 订单生成
- 订单`去付款`和`确认收货`
- 订单支付: 使用支付宝进行支付，支付完毕后跳回订单页面
- 大部分页面的错误信息提示由alert弹窗改为全局弹框
- **邮件功能实现**
- **MD5加密密码存储**
- **支付宝沙箱支付**
