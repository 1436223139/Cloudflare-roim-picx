# roim-picx

### 一款基于Cloudflare的Worker、R2、Pages实现的图床应用，具有以下特点：

* 10GB的免费存储空间
* 每月300W次的不计流量的图片访问，每天10W的限制。
* 每月100W次的图片上传次数
* 不需要自己购买服务器，克隆代码后部署CloudFlare即可使用。
* 独立部署不需要担心被第三方删除数据。

### 已实现功能

* 图片批量上传
* 图片列表查询
* 图片删除
* 目录创建
* 按目录查询
* 链接地址点击复制
* 简单的身份认证功能，进入管理页面需要授权

### 使用教程

1. Fork 项目到自己的 GitHub
2. 创建 Page 项目
3. 输入编译参数

    1. 框架预设：无
    2. 构建命令：`npm run build`
    3. 输出目录：`dist`

4. 完成创建
5. 设置环境变量

    1. `AUTH_TOKEN`：授权码，这个可以自定义填写，后面页面登录需要用到
    2. `COPY_URL`：复制的路径，如无，则输入`page域名/rest`
    
6. 创建 KV 命名空间

在 "Workers 和 Pages" 创建 KV 命名空间。

7. 设置函数，KV 命名空间绑定

回到 cloudflare page，点击 "设置" → "函数" 中 "KV 命名空间绑定"。
   
8. 设置函数，绑定 R2

   变量名为：`R2`
   
9. 重新部署

---

项目fork自[roimdev/roim-picx](https://github.com/roimdev/roim-picx)
