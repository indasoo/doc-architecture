# 创建hadoop用户
useradd -d /home/hadoop -m hadoop

# 修改用户密码
passwd hadoop

# 添加免密sudo权限
vi /etc/sudoers

hadoop  ALL=(ALL) NOPASSWD:ALL
