# Django开发的教学网站

### 预览图

![](https://s1.ax1x.com/2018/01/28/pvX7RS.png)

> 关于配置：
在路径iMooc_django/iMooc/config中, 可以详细修改你的配置脚本
*   settings_db.py 数据库配置
*   settings_local.py 开发环境配置
*   settings_product.py 生产环境配置

> 关于环境配置：

#### Deploying on AWS Lightsail

1. launch a Ubuntu 20.04 instance
2. switch to root user  
`sudo -s`
3. check the python version  
`python3 -v`
4. check any exist pip  
`python3 -m pip --version`
```
/usr/bin/python3: No module named pip
```
5. do an update before install pip for python3 
`apt update`
and install pip by reference: https://pip.pypa.io/en/stable/installing/

    - fetch the package `curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py`
    - install for python3 `python3 get-pip.py`

6. install Django version 1.11.23 per project requirement  
`pip install Django==1.11.23`
7. install package management tool  
`pip install pipenv`

#### 进入项目目录
```shell
#cd iMooc_django
```
#### 使用pipenv安装依赖
```python
pipenv install
```
#### 安装很多必要却没有列出的依赖
```
pip3 install pymysql
pip3 install future
pip3 install django-crispy-forms
pip3 install captcha
pip3 install django-pure-pagination
pip install django-formtools
```
```
pip install  django-simple-captcha
```
//注意安装最后一个包会更新Django到最新版本，所以重新安装一下：  
`pip install Django==1.11.23`


#### 生成数据库迁移文件
```python
python3 manage.py migrate
```
#### 启动项目
```python
python3 manage.py runserver 0:8080
```

(访问浏览器localhost:8080端口可以查看)

> 关于部署：
```python
settings.py中 DEBUG = True -> DEBUG = False
```

