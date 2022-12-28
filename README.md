# sxhgb_docker  山西好干部在线学习

## 学习环境

docker 镜像
1. selenium_python:v4     自己 build
2. selenium/standalone-chrome:108.0  从 dockerhub 拉取

## 学习步骤

1. 安装 docker 和 docer compose

2. 下载本项目
   
   ```git clone https://github.com/tustxsfh/sxhgb_docker.git```

1. build selenium_python:v4 镜像(Dockerfile)
   
   ```
   cd ./sxhgb
   docker build . -t selenium_python:v4   
   ```

2. 从 docker-compose.yml 运行程序
   
   - 修改 docker-compose.yml 文件中环境变量
     
     ```
     environment:
     - SXHGB_USRNAME=×××××××         # username
     - SXHGB_PWD=×××××××             # password
     - SXHGB_NAME=××××               # name 
     - SXHGB_GOAL=100                 # 年度目标学时 
     ```
     
    - 运行
       
      ```
      docker compose up -d
      ```
      
3. api 说明

     - chaxun(name)  查询本年度学时
     
     - find_peixun() 下载专题培训url
     
     - find_course() 下载课程url
     
     - keicheng() 课程按顺序学习
     
     - kecheng_random() 课程随机学习
     
     - peixun() 专题培训按顺序学习
     
     - peixun_random() 专题培训随机学习
