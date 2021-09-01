Flippy 的 Openwrt 打包源码，主要用于制作 Phicomm N1、贝壳云、我家云、微加云、Amlogic S905x3、Amlogic S922x等一系列盒子的 openwrt固件。

一、制作材料：
1. Flippy预编译好的 Arm64 内核 (在 https://t.me/openwrt_flippy  及 https://pan.baidu.com/s/1BIjHHfi90Oa7Le91Q8gkOg 提取码：02im )
2. 自己编译的 openwrt rootfs tar.gz 包： default-rootfs.tar.gz 

二、环境准备
    
1. 需要把 Flippy预编译好的 Arm64 内核上传至 kernel 目录
2. 安装依赖 sudo apt install btrfs-progs dosfstools uuid-runtime parted gawk
3. git clone https://github.com/LiangJC-JS/mk_openwrt_firmware.git     
4. 把编译好的 default-rootfs.tar.gz 上传至 mk_openwrt_firmware/rootfs 目录中
5. cd mk_openwrt_firmware

   sudo bash mk_s905d_n1.sh && sudo chown $USER:$USER -R tmp/

   生成好的固件是 .img.gz 格式， 存放在 mk_openwrt_firmware/tmp 目录中，下载刷机即可

    
                 
