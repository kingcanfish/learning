# 接口文档
#### 除了登陆授权获取基本信息其他路由带上请求头
Authorization: Bearer
###
## 授权登陆获取基本信息
#### URL：/api/user/token
### POST
```
{
    "code":"CODE"
}
```
#### RETURN
```
{
    "status":-102, //code无效或过期
    "message":"CODE无效！"
}
{
    "status":-101, //缺少code
    "message":"用户登录需要凭证"
}
{
    "status":1,
    "message":"成功！"，
    "data":{
        "token":TOKEN
    }
}

```
