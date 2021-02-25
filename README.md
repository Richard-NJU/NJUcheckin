# 南京大学自动打卡

**仅供学习使用，请正确填报身体状况！**

## 简介
这个 repo 通过Github Action实现每日自动打卡。

## 说明
- 打卡时使用前一日地理位置信息，如位置变更请提前停止自动打卡，到新位置手动打卡一次的一天后再开启
- 未经充分测试，**不保证最终效果**。
- **仅供学习使用，请正确填报身体状况！**

## 使用说明
- fork 本代码库
- 配置 Setting-Secrets 添加
  - USERNAME:学号
  - PASSWORD:统一身份认证密码
  - RECEIVERMAILUSERNAME:接收邮件的邮箱
  - MAILUSERNAME:发送邮件的163邮箱
  - MAILPASSWORD:发送邮件的163邮箱的密码
- 在 Actions 页面，开启 Workflows
  - 选择 NJUcheckin, enable

### 注意
- 163邮箱应打开smtp接口，[参看](http://help.163.com/09/1223/14/5R7P3QI100753VB8.html)。
- secret设置如图所示 
  ![image-20210224220441723](http://img.yp51md.club/image-20210224220441723.png)
- 在work.yml中的cron可以设置你喜欢的打卡时间(UTC)。


## Acknowledgement & Reference
- 灵感来源于[复旦大学项目](https://github.com/yew/fudanDaily)
- 参考了这个[项目](https://github.com/StellarDragon/nju-health-report)的打卡策略，节省了大量时间！
