<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Zabbix4 老旧系统一键安装脚本说明</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft YaHei", Consolas, sans-serif;
        }
        body {
            background-color: #f6f8fa;
            padding: 32px;
            max-width: 1200px;
            margin: 0 auto;
        }
        h2 {
            color: #24292f;
            margin-bottom: 10px;
            font-size: 26px;
        }
        p.desc-title {
            font-size: 17px;
            color: #57606a;
            margin-bottom: 20px;
        }
        .code-example {
            background-color: #161b22;
            color: #e6edf3;
            border-radius: 8px;
            padding: 24px;
            line-height: 1.8;
        }
        .section-title {
            font-size: 18px;
            color: #58a6ff;
            margin: 18px 0 10px;
            font-weight: bold;
        }
        ul {
            padding-left: 22px;
            margin-bottom: 12px;
        }
        .warn-tip {
            color: #f0883e;
        }
        .ok-tip {
            color: #7ee787;
        }
    </style>
</head>
<body>
    <h2>HTML 示例</h2>
    <p class="desc-title">zabbix一键安装脚本：</p>
    <div class="code-example">
        <div class="section-title">📌 脚本定位</div>
        <p>脚本文件：zabbix4_install.sh，专门适配 CentOS7/RHEL7 老旧Linux服务器，解决新版Zabbix无法兼容低内核、老旧软件源的问题。</p>

        <div class="section-title">✅ 兼容环境说明</div>
        <ul>
            <li>操作系统：仅支持 CentOS 7 / RHEL 7（内核3.10，老机房物理机/老旧云主机）</li>
            <li>Zabbix版本：锁定 4.0 LTS 归档旧版，是老旧系统可稳定运行的最高版本</li>
            <li>配套软件栈：PHP7.2 + MariaDB5.7，规避新版PHP/MySQL的底层依赖冲突</li>
        </ul>

        <div class="section-title">⚙️ 脚本自动化功能</div>
        <ul>
            <li>系统校验：非CentOS7系统直接终止，防止误部署</li>
            <li>环境初始化：自动关闭防火墙、SELinux，适配内网机房环境</li>
            <li>源修复：替换阿里云镜像源，解决官方旧源失效404问题</li>
            <li>数据库自动化：一键创建Zabbix数据库、业务账号，兼容老旧MySQL语法</li>
            <li>参数调优：自动修改PHP运行参数，满足Zabbix4运行硬性要求</li>
            <li>服务管理：统一配置 Nginx、数据库、Zabbix服务开机自启</li>
        </ul>

        <div class="section-title">🖥️ 服务器使用步骤</div>
        <ul>
            <li>1. 将 zabbix4_install.sh 上传至服务器 root 目录</li>
            <li>2. 执行授权：chmod +x zabbix4_install.sh</li>
            <li>3. root权限运行脚本：./zabbix4_install.sh</li>
            <li>4. 部署完成后访问：http://服务器IP/zabbix</li>
        </ul>

        <div class="section-title">⚠️ 重要注意事项</div>
        <ul class="warn-tip">
            <li>仅支持纯净最小化安装的CentOS7，服务器已有Nginx/MySQL业务会被覆盖</li>
            <li>该Zabbix4版本无法平滑升级至Zabbix5/6/7，内核限制不兼容高版本</li>
            <li>服务器需要外网连通，用于下载镜像源与Zabbix安装包</li>
        </ul>

        <div class="section-title">🔐 默认账号信息</div>
        <ul class="ok-tip">
            <li>Zabbix前端登录：账号 Admin，密码 zabbix</li>
            <li>数据库业务账号：zabbix，密码 Zabbix@1234</li>
            <li>数据库管理员root密码：123456</li>
        </ul>
    </div>
</body>
</html>
