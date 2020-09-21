# ITalker

## 手机端即时通讯App
[iTalker-Web](https://github.com/Super262/iTalker-Web) is the web server for ITalker. 
## 概述：

开发一个APP或微信小程序，实现聊天室列表、进入聊天等功能，支持两台或多台手机之间的聊天，聊天类型可以是文本、语音、图片、视频和位置分享。设计数据库，用于保存用户信息及聊天内容。开发一个后台接口及网站，用于接收APP或小程序上传的数据，并可以通过网站展示聊天室信息、用户信息及聊天内容。

## 软件和硬件环境： 
Android Studio 3.4.1，IntelliJ IDEA 2019

## 原理和方法：
App使用Android Studio开发，后台接口使用Jersy框架搭建。

## 步骤：

### 一、 需求分析

App需要具备单聊和群聊的功能，并支持文件（视频、图片、语音等）的发送；后台网站能够将所用的数据清晰地展示出来。

### 二、 概要设计
App包含三个模块，分别是消息模块、聊天模块和联系人模块。消息模块展示最新收到的消息的内容；用户可在聊天模块中进行单聊或群聊；用户可在联系人模块添加新的联系人、创建群。网站可以展示所有聊天内容、所有的群信息和所有的联系人信息。

### 三、 设计App的界面和功能逻辑

#### 1. 权限申请界面

![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00001.png)

#### 2. 注册界面

![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00002.png)

#### 3. 登录界面

![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00003.png)

#### 4. 最新消息界面

![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00004.png)

#### 5. 群聊界面

选择一个群，可以开始群聊。单击右下角的“建群”按钮，可以创建一个群。

![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00005.png)
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00006.png)

#### 6. 联系人界面

点击右下角的添加联系人按钮，可以添加新的联系人；选择一个联系人，开始单聊，可以发送语音、图片和表情。点击任意一个联系人的头像，可以查看他（或她）的个人信息。
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00007.png)
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00008.png)

### 四、 设计后台接口

#### 1. 账号相关

```
login：用户登录
register：用户注册
bind：绑定用户ID
```

#### 2. 用户相关

```
user：修改用户信息
contact：获得联系人
follow：加好友
getUser：获取某一用户的信息
search：搜索联系人
```

#### 3. 消息相关
```
msg：接收一条消息
```
#### 4. 群相关
```
list：获取群消息
getGroup：获取群信息
```

### 五、 后台接口的关键代码
```
1. BaseService：所有service的基类
2. AccountService：账号服务
3. UserService：用户服务
4. GroupService：群服务
5. MessageService：消息服务
```
### 六、 数据库设计
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00009.png)

### 七、 管理网站的界面
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00010.png)
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00011.png)
![image](https://github.com/Super262/ITalker/blob/master/screenshots/pic00012.png)

### 八、 测试
App端发送消息、语音、表情和图片的功能是正常的。网站中目前实现的功能是正常的，不足的是没有实现聊天室信息详细展示。

## 体会：
在本次项目开发中，我尝试着使用Android Studio编写原生的Android应用。虽然遇到了很多问题，但这些问题帮助我更好地理解Java中的并发机制、内存管理和Android的四大组件。在进行数据库设计时，我尝试着在多个实体间建立联系，提高关系模式的完备性。
