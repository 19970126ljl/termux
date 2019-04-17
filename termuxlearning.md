# 在安卓机上使用linux的体验

## 安装termux（去官网下载或者com.termux_66.apk）

- 安装必要工具
  - pkg install wget
  - pkg install vim
  - pkg install apt-transport-https
- 升级系统
  - apt update
- 运行Linux系统
  - pkg install proot(输入termux-chroot后变模拟root，exit退回普通用户)
  - git clone https://github.com/YadominJinta/atilo
  - cd atilo
  - chmod +x atilo
  - ./atilo
- 电脑通过ssh登陆到termux（windows10为例）
 - 电脑端操作
   - 电脑端生成密钥（如果之前没有）
    - cd ~/.ssh/
    - adb push id_rsa.pub /sdcard/
    - 使用 xshell 登陆
  - termux操作
    - termux-setup-storage
    - cp /sdcard/id_rsa.pub ./
    - cat id_rsa.pub >> authorized_keys
    - apt install openssh
    - cd ~/.ssh
    - sshd(启动)
- 内网渗透，通过外网连接termux（详见Ngrok）

termux深入教程: https://www.sqlsec.com/2018/05/termux.html
