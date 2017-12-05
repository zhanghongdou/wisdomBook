> # 注册接口
>
> 测试：[ comfire.cn](http://www.comfire.cn)  
> 正式： [comfire.cn](http://www.comfire.cn)

## 前言

所有接口均有加密

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



