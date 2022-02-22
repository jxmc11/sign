# juejin_auto

# 掘金自动化操作

> 掘金自动化操作

## Github Actions 部署指南

### 一、Fork 此仓库

### 二、添加掘金cookie等环境变量
> 添加名为  **juejinCookie**、**suohaIndex**、**signTime**、**suohaTimes**的变量: Settings-->Secrets-->New secret  
  或者你也可以直接写到代码上去，也是一样的效果

| Secrets |  格式  |
| -------- | ----- |
| juejinCookie | 掘金的cookie,多账号请回车换行添加|
| suohaIndex |   需要十连抽的账号, 列子： 1,2,3,6  表示第1,2,3,6个账号需要十连抽,注意第一个账号是1不是0|
| signTime |   设置当天超过signTime后不签到， 例如10: 则10点后不执行签到,默认是9点后二次运行则不再执行签到操作|
| suohaTimes |   十连抽执行的次数|

### 四、自定义启动时间

编辑 **.github/workflows/run.yml**

找到 cron: 5 0,10,13 * * *

修改其中的10为你要的时间

需要运行的时间-8就是UTC时间

## 注意事项

1. 每天运行3次，默认运行时间为每天 8:05 18:05 21:05，可自行修改

2. 启动时间得是UTC时间!

3. 请各位在使用时Fork[主分支](https://github.com/jxmc11/juejing_sign/)，防止出现不必要的bug.
# juejing_sign
