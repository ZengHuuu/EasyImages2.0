![打赏作者](https://i1.100024.xyz/i/2019/06/15/1u713g.png
 "打赏作者")

![简单图床示例](https://i1.100024.xyz/public/data/2019/05/5ce6915f50a1a.png
 "简单图床示例")
![简单图床示例](https://i1.100024.xyz/public/data/2019/05/5cecf12575f6e.png
 "简单图床示例")

## EasyImage 简单图床
> 支持多文件上传,api上传,简单无数据库,返回图片url,markdown,bbscode,html的一款图床程序
演示地址： [https://img.545141.com](https://img.545141.com"https://img.545141.com")
之前一直用的图床程序是:[PHP多图长传程序2.4.3](http://www.mycodes.net/48/4925.htm "PHP多图长传程序2.4.3")
由于版本过老并且使用falsh上传，在当前html5流行大势所趋下，遂利用基础知识新写了一个以html5为默认上传并且支持flash,向下兼容至IE9。

<hr />

#### 功能支持：

- [x] 支持仅登录后上传
- [x] 支持设置图片质量
- [x] 支持上传图片转换为指定格式
- [x] 支持文字/图片水印 颜色透明度
- [x] 支持设置图片指定宽/高
- [x] 支持限制最低宽度/高度上传
- [x] 支持静态文件CDN/本地切换
- [x] 支持设置广告
- [x] 支持开启/关闭api上传
- [x] 在线管理图片(增、删、改、查)
- [x] 支持网站统计 请将统计代码放入:public/static/hm.js

#### 一年未更新了，这次带来了全新版本2.0！
- 在继承上个版本（1.6.4）的基础上进行了全新优化
- 修复上传经常失败的问题
- 删除一些不常用但会增加功耗的过程 （删除的在下边会有标记）
- 全新的压缩 将文件继续缩小
- 全新的目录系统，精简代码
- 设置仅允许在config.php修改，注释更加明了，即使没有代码基础也可以操作
- 增加新的文件管理系统


#### 注意：

1. 安装之前先使用浏览器访问check.php检查扩展是否都安装！
2. 使用前请注意先修改config.php中的domain域名。
3. 请将所有文件必须赋予0777权限，执行用户设置www权限
4. 安装正常后请修改登录管理密码！
5. 如果无法登陆管理界面或上传图片，请先打开check.php检查扩展或者使用phpinfo检查。
6. 可以使用浏览器的 F12调试模式->console查看错误
7. 如果对php不太熟悉的话，不要将图床程序放置于二级目录
8. js不要设置分片上传大小，此会导致部分图片上传失败。
9. 默认我会给你设置成最优方案，api上传默认关闭
10. 下载源码后可以删除一些文件：README.md,check.php,LICENSE
11. 欢迎加群：[623688684](https://shang.qq.com/wpa/qunwpa?idkey=3feb4e8be8f1839f71e53bf2e876de36afc6889b2630c33c877d8df5a5583a6f)

#### api上传示例：
参数：

| 参数名称 | 类型 | 是否必须 | 说明 |
| :------------: | :------------: | :------------: | :------------: |
| file | file | 是 | 表单名称 |

html form上传示例:
```html
<form enctype="multipart/form-data" method="POST" action="https://img.545141.com/file.php">
        <label>选择文件</label>
        <input type="file" name="file">
        <input type="submit" value="提交">
</form>
```
api上传成功后返回json：
```json
{"result":"success","url":"https:\/\/img.545141.com\/public\/data\/2019\/05\/5ce64172d24fa.png"}
```
如果关闭api上传，则什么都不显示。

#### 更新日志
* 2021-03-28 v2.0.2.1
- 更新管理程序，修复部分漏洞
- 修复不能等比例缩小图片 
- 支持php8

* 2019-6-26 v2.0.2.0
- 精简压缩代码，使得不再压缩后反而变大
- 删除异域上传功能，不再支持异域上传
- 修复开启登录后无法粘贴密码
- 后台控制上传数量,上传格式
- 其他一些优化

* 2019-6-14 v2.0.1.9

- 增加复制链接按钮
- 增加暂停上传按钮
- 增加QQ截图，剪切板上传
- 增加文字/图片水印透明度
- 恢复开启/关闭api上传
- 恢复支持水印文字颜色
- 恢复支持远程上传图片
- 修复安装时候的权限
- 修复管理无法多选的问题
- 修复上传透明png背景变为纯黑的问题
- 修复成功上传图片但前端无法获取链接
- 修复在centos64 lnmp1.6 php7.1环境下的图片信息读取问题
- 修改图片压缩方式，速度更快，相比之前提高5倍以上
- 更改管理路径
- 更改上传路径，文件名更短
- 更改上传显示方式为缩略图
- 关闭添加图片后自动上传
- 纪念一下2019年，将版本号改为2.0.1.9

* 2019-5-23 v2.0
- 在继承上个版本（1.6.4）的基础上进行了全新优化
- 修复上传经常失败的问题
- 删除一些不常用但会增加功耗的过程
- 全新的压缩 将文件继续缩小
- 全新的目录系统，精简代码
- 设置仅允许在config.php修改，注释更加明了，即使没有代码基础也可以操作
- 增加新的文件管理系统，感谢 tinyfilemanager
- ~~支持文字/图片水印 可自定义文字颜色~~
- ~~支持文字水印背景颜色~~
- ~~支持文字水印透明度~~
- ~~支持删除远程上传文件~~ -> 不再支持删除远程文件
- ~~(支持开启/关闭api自定义文字水印)~~
- ~~支持删除自定义删除图片(仅管理员)~~

<hr />

* 2018-8-17 v1.6.4
- 支持删除远程上传文件
- 更改字体
- 添加api/远程上传 标识
* 2018-8-16 v1.6.3
- 支持开启/关闭api上传(支持开启/关闭api自定义文字水印)
- 修复权限错误
- 修复二级目录引入错误

* 2018-8-8 v1.5.3
- 添加上传图片至远程主机
- 修复逻辑

* 2018-8-6 v1.4.3
- 添加网站统计
- 添加删除上传文件
- 调整config.php

* 2018-8-5 v1.4.2
- 添加仅登录后上传
- 修复一处逻辑错误
- 修复一个漏洞

* 2018-8-4 v1.3.2
- 添加广告设置
- 完善引入机制

* 2018-8-3 v1.2.2
- [重要]修复水印图片不能添加
- 添加随机浏览上传图片 可以设定浏览数量和关闭浏览
- 优化代码，删除无用文件
- 完善一键CDN静态文件

* 2018-08-02 v1.1.2
- [重要] 修复gif上传添加水印成静态的问题
- 修复文字水印背景色不显示问题
- 修复在linux下的权限错误
- 一些优化更改

* 2018-08-01 v1.0.1
- 更改相关文件目录
- 优化代码

* 2018-07-30 v1.0.0
- 最初模型

#### 兼容性
文件上传视图不支持IE9以下的浏览器,api不限制。建议php5.6及以上版本,需要服务器支持Fileinfo, iconv ,zip和mbstring扩展,如果缺失会导致无法访问管理面板以及上传图片。

文件上传视图提供文件列表管理和文件批量上传功能，允许拖拽（需要 HTML5 支持）来添加上传文件，支持上传大图片，优先使用 HTML5，旧的浏览器自动使用Flash和Silverlight的方式兼容。
<hr />

 - 感谢: [verot](https://www.verot.net "verot" )提供非常好用的class.upload.php上传类
 - 感谢: [ZUI](http://zui.sexy/ "ZUI" ) 提供css框架
 - 感谢:[tinyfilemanager](https://github.com/prasathmani/tinyfilemanager "tinyfilemanager" ) 提供的文件管理
 - 本源码遵循 GNU Public License