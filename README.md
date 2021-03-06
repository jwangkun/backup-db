<a href="https://github.com/jeessy2/backup-db/releases/latest"><img alt="GitHub release" src="https://img.shields.io/github/release/jeessy2/backup-db.svg?logo=github&style=flat-square"></a>
# 数据库备份工具 [English](README-EN.md)
  原理：在原生的docker镜像基础上，加入一备份工具，增强备份功能。
  提供postgres, mysql5, mysql8镜像，可直接使用，如有需要请提issues。
  - [X] 支持自定义命令
  - [x] 支持多个项目备份，最多16个
  - [X] 支持备份后的文件存入另一台服务器
  - [X] 服务端每日10点检查上传的备份文件
  - [X] 每日凌晨自动备份
  - [X] 可设置备份文件最大保存天数
  - [x] 网页中配置，简单又方便
  - [x] 网页中方便快速查看最近50条日志
  - [x] 可设置登陆用户名密码，默认为空
  - [x] 邮件通知
  - [x] 钉钉通知

## docker中使用
  - 运行docker容器。参考[https://github.com/jeessy2/backup-db/releases](https://github.com/jeessy2/backup-db/releases)
  - 登录 http://your_docker_ip:9977 并配置
    ![avatar](https://raw.githubusercontent.com/jeessy2/backup-db/master/backup-db-web.png)

## 说明
  - v1版本开始发生重要变化，不兼容0.0.x
  - v1后开始使用web方式来配置
  - 如要加入https，可通过nginx代理

## 钉钉通知
  - 钉钉电脑端->群设置->智能群助手->添加机器人->自定义
  - 只勾选 `安全设置->加签`
  - 复制 `WebHook` `加签` 内容到web中

## Release
```
git tag v0.0.x -m "xxx" 
git push --tags
```