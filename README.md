# 概述

随着直播的越来越普及，企业、教育中随时开启直播的场景越来越多，红鲸直播赋能企业、教育各种应用随时开启直播，让您的应用轻松插上即时直播的翅膀。

红鲸直播SDK是自带UI功能的直播SDK，具有如下特点：
1. 集成简单：用户只需简单几行代码就可以拥有私有化部署的直播功能；
2. 功能全面：具备了直播创建，共享桌面，录制，聊天室等直播的常用功能；
3. 平台能力稳定：直播基于稳定的RTC平台构建，具备网络切换，断网重连，弱网重传等功能。支持H264和AV1等先进的编码方式，保证了低码率和画质。
4. 私有化部署：满足企业安全需求，方便企业资产结算。

# 集成必读

在集成SDK之前，需要做如下提前准备：
1. 需要部署好直播服务端，确认好直播服务器的地址和端口;
2. 集成本SDK的项目需要有用户体系，调用SDK时需要指定用户名，用户ID，用户头像地址这些用户信息；
3. 集成直播功能时，集成本SDK的项目需要提供创建直播或者进入直播间的入口交互能力，如果是进入直播间则需要提供直播号;

# 快速开始

## 集成准备

### 开发环境要求

- Chrome浏览器
- 集成项目必须支持hash路由

## 手动集成步骤
### 导入SDK文件夹
将SDK文件夹中的内容拷贝至能访问的目录中, 确保目录中<code>*.html</code>文件能被访问到<br/> 
例如访问地址: <br/>
直播链接:<code>http://localhost:3000/index.html</code>


## 集成代码
### 创建直播
```
  window.redwhale.live.init({
    entry: 'create', // 创建直播
    user: {
      userId: 'xxxx', // 用户ID 必填
      userName: 'xxxxx', // 用户名称 必填
      avatar: 'xxxx', // 用户头像 可选
    },
    severUrl: '' // 直播服务地址 必填
  })
```
### 进入直播间
```
  window.redwhale.live.init({
    entry: 'join', // 进入直播间
    user: {
      userId: 'xxxx', // 用户ID 必填
      userName: 'xxxxx', // 用户名称 必填
      avatar: 'xxxx', // 用户头像 可选
    },
    severUrl: '' // 直播服务地址 必填
  })
```
将上述代码拷贝至<code>index.html</code>中，代码位置放置于页面尾部
### 示例代码

```
<script>
  window.redwhale.live.init({
    entry: 'create', // 创建直播
    user: {
      userId: '1000', // 用户ID 必填
      userName: '用户名称', // 用户名称 必填
      avatar: '头像地址', // 用户头像 可选 示例 https://xxxxxx
    },
    severUrl: '' // 直播服务地址 必填
  })
</script>
```