> ## 意见反馈 {#前言}
>
> ## **请求路径**

/Home/user/feedback

> ## 请求方式 {#请求}

【POST】

> ## 参数： {#请求}

| 参数 | 类型 | 说明 |
| :---: | :---: | :---: |
| uid | String | 用户的uid |
| content | String | 反馈的内容 |

> ## 返回值示例： {#请求}

```
@apiSuccessExample {json} Success-Response:
     *     {
     *           "status": 1,
     *           "version": 1.0,
     *           "info": "反馈成功",
     *           "data": {}
     *  
     *      }
     * @apiErrorExample {json} Error-Response:
     *     {
     *           "status": 0,
     *           "version": 1.0,
     *           "info": "反馈失败"
     *           "data": {}
     *      }
```



