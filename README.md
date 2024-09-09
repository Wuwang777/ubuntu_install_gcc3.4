### 由于操作系统课程需要安装gcc-3.4
### 踩了许多坑后总结出的一系列命令，只需要按顺序执行即可
### 测试环境为Ubuntu20.04-beta-desktop-amd64

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/gcc-3.4-base_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i gcc-3.4-base_3.4.6-6ubuntu3_amd64.deb

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/gcc-3.4_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i gcc-3.4_3.4.6-6ubuntu3_amd64.deb 

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/cpp-3.4_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i cpp-3.4_3.4.6-6ubuntu3_amd64.deb 

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/g++-3.4_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i g++-3.4_3.4.6-6ubuntu3_amd64.deb

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/libstdc++6-dev_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i libstdc++6-dev_3.4.6-6ubuntu3_amd64.deb

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/g77-3.4_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i g77-3.4_3.4.6-6ubuntu3_amd64.deb

wget http://old-releases.ubuntu.com/ubuntu/pool/universe/g/gcc-3.4/libg2c0-dev_3.4.6-6ubuntu3_amd64.deb

sudo dpkg --force-depends -i libg2c0-dev_3.4.6-6ubuntu3_amd64.deb

sudo apt-get install libc6-dev

sudo apt --fix-broken install -y

sudo cp /lib/x86_64-linux-gnu/libgcc_s.so.1 /lib/libgcc_s.so.1

### 以下内容用vim在~/.bashrc最后添加 记得source ~/.bashrc 使环境变量生效
## export LIBRARY_PATH=/usr/lib/x86_64-linux-gnu:$LIBRARY_PATH
