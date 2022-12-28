# sxhgb_docker

## 山西好干部在线学习

## 学习环境

- docker 镜像
  1. selenium_python:v4     自己 bulid
  2. selenium/standalone-chrome:108.0  从 dockerhub 拉取

## 学习步骤

1. 安装 docker 和 docer compose

2. 下载本项目
   
   - git clone https://github.com/tustxsfh/sxhgb_docker.git

3. build selenium_python:v4 镜像(Dockerfile)
   
   ```
   cd ./sxhgb
   docker build . -t selenium_python:v4   
   ```

4. 从 docker-compose.yml 运行程序
   
   - 修改 docker-compose.yml 文件中环境变量
     
     ```
     environment:
     - SXHGB_USRNAME=×××××××         # username
     - SXHGB_PWD=×××××××             # password
     - SXHGB_NAME=××××               # name 
     ```
     
     - 运行
       
       ```
       docker compose up -d
       ```
# sxhgb
