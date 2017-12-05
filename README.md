> # 注册接口 {#register}
>
> 测试：[ comfire.cn](http://www.comfire.cn)  
> 正式： [comfire.cn](http://www.comfire.cn)

## 前言 {#前言}

所有接口均有加密（使用AES加密，然后md5二次加密）

## 请求方式 {#请求}

【POST】

## 参数 {#请求}

> | 参数名 | 类型 | 说明 |
> | :--- | :--- | :---: |
> | phone | String | 手机号 |
> | password | String | 密码（需要加密） |
> | nickname | String | 昵称 |
> | client | Int | 客户端类型:1.web  2.android  3.ios  4.wap |
> | devVer | String | 设备型号 |
> | sysVer | String | 手机系统版本型号 |
> | appVer | String | app版本号 |
> | loginCity | String | 注册城市 |
> | sign | String | 加密之后的参数 |
> | idfv\_mark | String | iOS端传的idfv |
> | ease\_username | String | 环信的username（id） |

返回值示例：

```
@apiSuccessExample {json} Success-Response:
     *     {
     *           "status": 1,
     *           "version": 1.0,
     *           "info": "注册成功",
     *           "data": {}
     *      }
     * @apiErrorExample {json} Error-Response:
     *     {
     *           "status": 0,
     *           "version": 1.0,
     *           "info": "该手机号已被注册"
     *           "data": {}
     *      }
```

> # 登陆接口

## 请求方式 {#请求}

【POST】

## 参数 {#请求}

> | 参数名 | 类型 | 说明 |
> | :--- | :--- | :---: |
> | phone | String | 手机号 |
> | password | String | 密码（需要加密） |
> | client | Int | 客户端类型:1.web  2.android  3.ios  4.wap |
> | devVer | String | 设备型号 |
> | sysVer | String | 手机系统版本型号 |
> | appVer | String | app版本号 |
> | loginCity | String | 注册城市 |
> | sign | String | 加密之后的参数 |
> | idfv\_mark | String | iOS端传的idfv |

返回值示例：

```
@apiSuccessExample {json} Success-Response:
     *     {
     *           {
    "status": 1,
    "version": 1.0,
    "info": "登录成功”,//登陆失败的情况：1.账号输入错误，没有此用户    2.密码输入错误，请重新输入密码
    "data": {
        "id": 4,
        “uid”:“”，用户ID
        “login_token”:“”服务端生成，用来检验是不是同一个设备登陆
        “sex”:“”用户的性别
        “school”：毕业院校
        “occupation”：职业
        "nickname": "佚名”,用户的昵称
        "avatar": "http://www.english.com/uploads/user/avatar.jpg”,头像
        "email": null,用户的邮箱
        “islogin”：0，  是否签到
        “loginday”:10,   连续签到的天数
        “loginallday”:20，   本月签到的总天数
        "ease_username":环信账号
        }
}
     *      }
     * @apiErrorExample {json} Error-Response:
     *     {
     *           "status": 0,
     *           "version": 1.0,
     *           "info": "登陆失败"
     *           "data": {}
     *      }
```



