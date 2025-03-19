# campus-canteen-ordering
数据库原理课程作业：实现校园食堂点餐系统
---

<p align="center">
    <a><img src="https://img.shields.io/badge/status-updating-brightgreen.svg"></a>
    <a><img src="https://img.shields.io/badge/Python-3.8-FF1493.svg"></a>
    <a><img src="https://img.shields.io/github/repo-size/hewei2001/campus-canteen-ordering"></a>
    <a><img src="https://img.shields.io/github/license/hewei2001/campus-canteen-ordering"></a> 
</p>

# <p align="center">Campus Canteen Ordering System</p>

HITSZ 2021 年秋季学期「数据库设计」课程实验项目，基于 MySQL+Django 实现**校园食堂点餐系统**。


主要环境：

- PowerDesigner
- MySQL Workbench 8.0 CE
- Python 3.8
- Django 3.2.8
- BootStrap 3.3.7
- Django-simpleui

## 系统功能 :snake:

<div align="center">
	<img src="img/func1.png" alt="管理员模块" align="center" width=80% />
	<img src="img/func2.png" alt="用户模块" align="center" width=80% />
</div>

## 项目结构 :pencil:

```
django_CCOS
 ├── canteen				//app1
 ├── customer				//app2
 ├── dish				//app3
 │   ├── admin.py
 │   ├── apps.py
 │   ├── migrations
 │   ├── models.py			//数据库模型
 │   ├── tests.py
 │   ├── urls.py
 │   ├── views.py			//实现的视图
 │   └── __init__.py
 ├── django_CCOS
 │   ├── asgi.py
 │   ├── settings.py			//配置文件
 │   ├── urls.py
 │   ├── wsgi.py
 │   └── __init__.py
 ├── manage.py
 ├── media				//图片文件
 │   └── images
 ├── static				//样式文件
 │   ├── bootstrap-3.3.7-dist
 │   ├── css
 │   └── js
 └── templates				//页面模板 
     ├── base.html
     ├── canteen
     │   ├── canteen_base.html
     │   ├── canteen_list.html		//食堂展示
     │   └── shop_list.html		//窗口展示
     ├── customer
     │   ├── index.html
     │   ├── information.html		//完善用户信息
     │   ├── login.html			//登录界面
     │   ├── logout.html		//登出界面
     │   ├── register.html		//注册界面
     │   └── show_info.html		//个人
     └── dish
         ├── dish_base.html
         ├── dish_list.html		//菜品展示
         └── my_order.html		//我的订单
```

## 快速开始 :rocket:

1. 初始化：

   - 克隆本项目

   - 卸载原依赖 `pip uninstall -y -r requirement.txt`

   - 配置新依赖 `pip install -r requirements.txt`

2. 数据库准备：

   - 打开 MySQL Workbench 服务器，创建本地数据库 `create database django_CCOS`

   - 项目参数修改：打开 settings.py 配置文件，找到 MySQL 自定义参数，修改为你自己的配置

4. 项目启动，进入项目 `django_CCOS` 目录，执行：
   - `python manage.py makemigrations`
   - `python manage.py migrate`
   - `python manage.py runserver`
   
5. 前端访问：http://127.0.0.1:8000

5. 后台访问：http://127.0.0.1:8000/admin
   - 创建管理员：`python manage.py createsuperuser`
   - 自行添加食堂、窗口、菜品，否则初始不显示




