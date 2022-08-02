### 技术选型：

* JDK8
* MySQL
* Spring-boot
* Spring-data-jpa
* Shiro
* Lombok
* Freemarker
* Bootstrap
* SeaJs

    
### 版本(4.0)更新内容：
    1. 新增 <@layout.extends name="xxx"></layout.extends> 标签, 用于进入模板文件, 解决主题开发时各种路径带入主题名的问题
    2. 新增 <@layout.block name="header"></layout.block> 标签, 用于模板的占位, 可配合`layout.put`替换指定block区域内容,
    3. 新增 <@layout.put block="contents" type="APPEND"></layout.put> 标签, 用户替换模板内容块, 丢弃freemarker变量传递, 增强主题可维护性
    4. `layout.put`中的type 支持替换类型: APPEND, PREPEND, REPLACE
    5. 调整`default`, `classic`主题, 使用新的主题开发方式
    6. `建议MySQL版本5.7`, 如果不能满足5.7+可自行去除flyway依赖及代码

### 版本(3.5)更新内容：
    1. 文件存储目录可配置, 见 site.location, 默认为 user.dir
    2. 支持在${site.location}/storage/templates 目录下扩展自己的主题(${site.location}具体位置见启动日志)
    3. 后台未配置对应第三方登录信息时, 前端不显示对应的按钮
    4. 模板优化
    5. 后台配置主题改为自动从目录中加载
    6. 新增markdown编辑器, 可在后台选择tinymce/markdown

### 版本(3.0)更新内容：
    1. 新增开关控制(注册开关, 发文开关, 评论开发)
    2. 后台重写, 替换了所有后台页面功能更完善
    3. 上传图片添加更多支持(本地/又拍云/阿里云/七牛云), 详情见后台系统配置
    4. 升级为spring-boot2
    5. 调整模板静态资源引用,方便扩展
    6. 表名调整, 旧版本升级时请自行在数据库重命名, 详情见change.log
    7. 重写了config(改为options), 可在applicaiton.yaml设置默认配置, 启动后将以options中配置为准
    8. 支持后台设置主题
    9. 去除了本地文件上传目录配置, 改为自动取项目运行目录(会在jar同级目录生成storeage和indexes目录)
    10. 替换表单验证插件, 评论表情改为颜文字
    11. 我的主页和Ta人主页合并
    12. 优化了图片裁剪功能
    13. 支持Docker, 详情见 https://hub.docker.com/r/langhsu/mblog
    14. 邮件服务后台可配
    15. 新增标签页
    16. 新增注册邮箱验证开关(需要手动删除之前的 mto_security_code 表)
