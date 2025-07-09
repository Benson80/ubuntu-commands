## 🐧 Ubuntu 常用命令速查表

> 📁 文件名建议：`ubuntu-commands-cheatsheet.md`

------

### 🧠 系统信息

| 命令             | 功能描述             |
| ---------------- | -------------------- |
| `uname -a`       | 查看内核/系统架构    |
| `lsb_release -a` | 查看发行版信息       |
| `hostnamectl`    | 查看主机名和系统信息 |
| `uptime`         | 系统运行时间         |
| `free -h`        | 查看内存使用情况     |
| `df -h`          | 查看磁盘空间         |
| `du -sh *`       | 当前目录文件夹大小   |



------

### 🌐 网络相关

| 命令                   | 功能描述           |
| ---------------------- | ------------------ |
| `ip a`                 | 查看IP地址         |
| `ip r`                 | 查看路由表         |
| `ss -tuln`             | 查看监听端口       |
| `ping -c 4 baidu.com`  | 网络连通性测试     |
| `traceroute baidu.com` | 路由追踪（需安装） |
| `dig baidu.com`        | DNS查询（需安装）  |
| `curl ifconfig.me`     | 查看公网IP地址     |



------

### 👤 用户管理

| 命令                      | 功能描述         |
| ------------------------- | ---------------- |
| `whoami`                  | 当前用户名       |
| `id`                      | 当前UID/GID      |
| `adduser 用户名`          | 添加用户         |
| `passwd 用户名`           | 修改密码         |
| `deluser 用户名`          | 删除用户         |
| `usermod -aG sudo 用户名` | 添加用户到sudo组 |
| `groups 用户名`           | 查看用户所属组   |



------

### 🔐 权限与文件

| 命令                       | 功能描述       |
| -------------------------- | -------------- |
| `ls -l`                    | 查看文件权限   |
| `chmod +x file.sh`         | 增加可执行权限 |
| `chown 用户:用户组 文件名` | 修改属主       |
| `find / -name "*.conf"`    | 查找配置文件   |
| `cp -a /src /dst`          | 保留权限复制   |
| `rsync -av src/ dst/`      | 同步目录       |



------

### 📦 软件包管理（APT）

| 命令                             | 功能描述   |
| -------------------------------- | ---------- |
| `sudo apt update && apt upgrade` | 更新系统   |
| `sudo apt install 软件名`        | 安装软件   |
| `sudo apt remove 软件名`         | 卸载软件   |
| `apt search 软件名`              | 搜索包     |
| `dpkg -l                         | grep 包名` |
| `sudo apt-get install -f`        | 修复依赖   |



------

### ⚙️ 服务管理（systemd）

| 命令                      | 功能描述     |
| ------------------------- | ------------ |
| `systemctl status nginx`  | 查看服务状态 |
| `systemctl start nginx`   | 启动服务     |
| `systemctl stop nginx`    | 停止服务     |
| `systemctl restart nginx` | 重启服务     |
| `systemctl enable nginx`  | 设置开机自启 |
| `journalctl -u nginx`     | 查看服务日志 |



------

### 🧮 进程与资源管理

| 命令              | 功能描述                 |
| ----------------- | ------------------------ |
| `ps aux           | grep nginx`              |
| `top` / `htop`    | 实时资源监控（htop更好） |
| `kill -9 PID`     | 强制结束进程             |
| `pkill -f 进程名` | 按名称杀死进程           |
| `nice -n 10 命令` | 设置优先级运行           |



------

### 🧱 磁盘与挂载

| 命令                   | 功能描述     |
| ---------------------- | ------------ |
| `lsblk`                | 查看磁盘结构 |
| `df -h`                | 查看挂载情况 |
| `mount /dev/sdb1 /mnt` | 手动挂载     |
| `umount /mnt`          | 卸载挂载点   |
| `blkid`                | 查看UUID     |



------

### 🧾 日志查看

| 命令                        | 功能描述     |
| --------------------------- | ------------ |
| `dmesg                      | tail -n 20`  |
| `journalctl -xe`            | 系统错误日志 |
| `tail -f /var/log/syslog`   | 实时系统日志 |
| `tail -f /var/log/auth.log` | 登录认证日志 |



------

### 🛡️ 防火墙与安全

| 命令                     | 功能描述                     |
| ------------------------ | ---------------------------- |
| `sudo ufw status`        | 查看UFW防火墙状态            |
| `sudo ufw allow 22`      | 开放SSH端口                  |
| `sudo ufw enable`        | 启用防火墙                   |
| `fail2ban-client status` | 查看Fail2Ban状态（如已安装） |



------

### 🔧 系统调试

| 命令                  | 功能描述               |
| --------------------- | ---------------------- |
| `lsof -i`             | 查看端口使用           |
| `netstat -tulnp`      | 查看端口监听（需安装） |
| `strace -p PID`       | 跟踪系统调用           |
| `nc -zv 127.0.0.1 80` | 测试端口连通性         |
| `time 命令`           | 测试命令耗时           |

bash <(curl -fsSL https://benson80.eu.org/scripts/ubuntu-commands.sh)
![image](https://github.com/user-attachments/assets/4a101d29-d48e-4d50-9406-48fb6b9daf26)
