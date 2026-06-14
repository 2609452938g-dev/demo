# Zabbix4 老旧系统一键安装脚本
仓库文件说明：
1. `zabbix4_install.sh`：CentOS7/RHEL7 专用 Zabbix4.0 自动化部署脚本，适配低内核老旧服务器
2. `index.html`：脚本功能说明静态展示页面，在线查看适配范围、使用步骤、注意事项

## 脚本核心适配老旧系统特性
- 仅兼容 CentOS7 / RHEL7（内核3.10），高版本系统会校验拦截
- 锁定 Zabbix4.0 LTS 归档版，配套 PHP7.2 + MariaDB5.7，规避新版依赖冲突
- 自动替换国内阿里云镜像源，修复官方老源失效问题
- 一键完成防火墙/SELinux、数据库、Nginx、PHP、Zabbix全流程配置

## 使用方法
1. 上传脚本至服务器 root 目录
2. 授权执行：`chmod +x zabbix4_install.sh`
3. root 用户运行：`./zabbix4_install.sh`
4. 部署完成访问：`http://服务器IP/zabbix`

## 账号信息
- Zabbix前端：Admin / zabbix
- 数据库zabbix业务用户：zabbix / Zabbix@1234
- MySQL root管理员：123456

## ⚠️ 注意事项
1. 仅支持纯净最小化 CentOS7，已有Nginx/MySQL业务会被覆盖
2. Zabbix4 无法平滑升级至 5/6/7 高版本
3. 服务器需可连通外网下载镜像源
