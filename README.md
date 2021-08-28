# Centos-rasa-install

# 
# 1.安装yum

1. wget http://yum.baseurl.org/download/3.2/yum-3.2.28.tar.gz  
2. tar xvf yum-3.2.28.tar.gz  
3. cd yum-3.2.28  
4. sudo apt install yum  
5. yum update

# 2.安装docker

https://docs.docker.com/engine/install/centos/  

# 3.安装rasax

1. Download  
curl -sSL -o install.sh https://storage.googleapis.com/rasa-x-releases/0.42.0/install.sh  
2. Install 
sudo bash ./install.sh  
3. Start  
cd /etc/rasa  
sudo docker-compose up -d  
4. Access  
cd /etc/rasa  
sudo python3 rasa_x_commands.py create --update admin me <PASSWORD>  

# 4.安装rasa  

1. pip3 install -U pip  
2. pip3 install rasa  
3. rasa init  
3. nohup rasa run -m models --enable-api --cors "*"  --debug &  


# 5.安装gcc++

sudo apt-get install build-essential 

# 6.安装安装PCRE库
1.  cd /usr/local/ 
2.  wget http://jaist.dl.sourceforge.net/project/pcre/pcre/8.33/pcre-8.33.tar.gz  
3.  tar -zxvf pcre-8.36.tar.gz  
4.  cd pcre-8.36  
5.  ./configure  
6.  make && make install  

# 7.安装SSL库  
1. cd /usr/local/  
2. wget http://www.openssl.org/source/openssl-1.0.1j.tar.gz  
3. tar -zxvf openssl-1.0.1j.tar.gz  
4. cd openssl-1.0.1j  
5. ./config  
6. make && make install  

# 8.安装zlib库存  
1. cd /usr/local/  
2. wget http://zlib.net/zlib-1.2.11.tar.gz  
3. tar -zxvf zlib-1.2.11.tar.gz  
4. ./configure  
5. make && make install

# 9.安装nginx


1. cd /usr/local/  
2. wget http://nginx.org/download/nginx-1.8.0 .tar.gz  
3. tar -zxvf nginx-1.8.0.tar.gz  
4. cd nginx-1.8.0  
5. ./configure  
6. make && make install



Ubuntu18.04编译Nginx报错objs/Makefile:440: recipe for target ‘objs/src/core/ngx_murmurhash.o’ failed  

解决方案：Maakefile文件（/nginx/objs/Makefile），将gcc参数中的-Werror去掉 再重新make即可
