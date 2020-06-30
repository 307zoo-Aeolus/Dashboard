# 前后端分离基础

## 什么是前后端分离？
[https://blog.csdn.net/fuzhongmin05/article/details/81591072](https://blog.csdn.net/fuzhongmin05/article/details/81591072)
简单来说就是实现了前后端互为黑箱。前端开发人员不必关心后端用的是什么，只需要拿到一个url作为接口即可。后端也不用学前端框架。

## Restful接口
概念：[https://www.restapitutorial.com/](https://www.restapitutorial.com/)
方法：[https://spring.io/guides/gs/rest-service/](https://spring.io/guides/gs/rest-service/)

## Note
前端需要后端提供的接口主要有：
用户注册（邮箱验证）、登录、修改密码、找回密码

## 使用Django REST Framework创建RESTful接口
入门：
[https://blog.stdioa.com/2017/03/DRF-demo/](https://blog.stdioa.com/2017/03/DRF-demo/)
[https://www.jianshu.com/p/2538e8aa1ead](https://www.jianshu.com/p/2538e8aa1ead)
文档：
[https://www.django-rest-framework.org/](https://www.django-rest-framework.org/)
参考视频：
[https://www.youtube.com/watch?v=Uyei2iDA4Hs](https://www.youtube.com/watch?v=Uyei2iDA4Hs)

## 简介
### 类比Django来介绍
如果在 Django 中写一个页面，你需要：
1.	在 urls.py 中注册 view；
2.	在 views.py 中编写 view；
3.	在 templates 文件夹中编写模板。
相对地，如果使用 DRF 创建一组 API，你需要：
1.	在 urls.py 中定义并注册 router；
2.	在 views.py 中定义 ViewSet；
3.	在 serializers.py 中定义 serializer.
这里，urls.py负责路由（说明访问某个url对应调用哪个函数），views.py负责后端逻辑处理（查询数据库、处理数据等操作都在这里），model.py负责定义数据库中的数据类型，serializer.py负责转换数据库中的Model Data（数据库中数据存储的类型）和JSON类型的数据。

### 实现一组api的基本流程
1.	在models.py中创建自己需要的数据模型
2.	创建serializers.py在其中写出适合的serializer类，能够正确的序列化与反序列化
3.	在views.py中写出合适的api类，只需要继承rest_framework中generics中的某个类，重写我们需要的方法实现合适的逻辑即可
4.	在urls.py中配置所需要的url

## 参考链接
1.  [RESTful架构详解](https://www.runoob.com/w3cnote/restful-architecture.html)
2.  [RESTful API 设计指南](http://www.ruanyifeng.com/blog/2014/05/restful_api.html)


