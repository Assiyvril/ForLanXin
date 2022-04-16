# Lan Xin's Dream

**He has a great dream**



## 上传简历的小程序

```mermaid
graph TB
A(开始)-->B{判断用户是否存在}-->|已存在|C[登录]
B-->|不存在|D[注册]
C-->E[更新简历 / 更新意向工作地点 / 更新工作状态]-->H[保存修改]
D-->F[制作简历 按照标准模板填写] -->G[选择意向工作地点]-->I[选择个人状态 求职/ 暂不求职]
C-->J[注销账户]-->K[确认注销]-->L[Delete data]-->M[End]
H-->M
I-->M
```

**简历信息包括：**

- 姓名
- 电话
- 学历
- 工作经历
- 照片
- 证书
- 工种
- et.al  #  待兰鑫添加





## 客户端，面向企业

### Instructions

- 预充值，余额随时可退款

- 普通客户已购买的项目不可退款

- 定制化高级客户根据订单完成情况退款
    - 例如某订单，需要10位安全员，10位资料员，支付了1000元。完成情况是5位资料员和5位安全员，退款500元

- 顶栏显示余额



### step1 注册

邀请注册，不开放

- 企业名称 unique =True
- 手机号
- 地址  选择 市区县街道，输入门牌号
- 使用人的 部门，姓名，职务
- 自定义ID unique=True

### step2 登录

ID & 密码登录， 手机号找回密码，或联系客服重置



### Step3 登陆后可查看：

#### Page1—— 普通客户

```mermaid
graph TB
A((普通客户/开始))-->B[选择项目所在地/市区县]-->C[各个工种所需人数]-->D[提交]
```

- 提交之后，显示所有可选人员

    - 每人为一个条目预览，显示姓名、学历、专业、工作经验
    - 条目点击可显示详情，点击购买
    - 购买该条目后在预览页面和详情页面看到联系方式
    - 条目添加复选框，便于批量购买

#### Page2 -- 普通客户 资产及订单管理

- 查看账户余额

- 退款
- 充值
- 查看已购买的订单项目
- 交易记录
- 个人资料管理/密码/更新手机号

#### Page3——定制化高级客户

```mermaid
graph TB
A((高级客户/开始))-->B[展示级别介绍/具体内容问兰鑫]-->C[选择项目所在地等信息]-->D[提交并支付]-->E[本公司将于xx小时内完成此业务/点此查看进度]-->F[End]
```

- 查看进度，eg:
    - 您的XX项目需要资料员6名，安全员7名，现已完成资料员3名，安全员4名

- 订单完成后，短信通知，并在登陆时首页提醒

#### Page4 定制化高级客户资产及订单管理

- 充值
- 余额
- 退款
- 个人资料管理
- 查看订单
    - 已完成订单显示详情
        - 订单记录详情
        - 完成情况
        - 是否有退款及退款详情
    - 进行中的订单显示进度

## 公司后台

**老板拥有所有权限**

- 订单处理
- 资源库展示、修改、添加
- 营业情况
- 注册客户信息

### 订单处理

权限：订单处理者



