# proxmox-dosthol
通过  WOL  唤醒 Proxmox  虚拟机 

Source/Credit: https://forum.proxmox.com/threads/update-wake-and-other-on-lan-for-vms-v0-3.26381/

- 1、更新软件包列表：
   apt-get update
- 2、 安装依赖：
   apt install gawk socat xxd
- 3、 复制 dosthold.sh dostholc.sh 到 /usr/local/bin，dosthol.service 到 /etc/systemd/system
- 3、 更改文件权限：
   
   chmod +s /etc/systemd/system/dosthol.service
   
   chmod +x /usr/local/bin/dosthold.sh
   
   chmod +x /usr/local/bin/dostholc.sh
- 4、 打开 dosthol 自动启动
   systemctl enable dosthol
- 5、 启动 dosthol
   systemctl start dosthol
