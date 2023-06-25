# 客户授权

---

## 授权登录

> 基础信息

**Path:** /api/channels/{{channelNo}}/auth-login

**Method:** POST

> 请求

**Headers:**

| name         | value                             | required | desc |
|--------------|-----------------------------------|----------|------|
| Content-Type | application/x-www-form-urlencoded | YES      |      |

**Body:**

| name   | type    | desc  |
|--------|---------|-------|
| param1 | string  | 参数1   |
| param2 | string  | 参数2   |
| param3 | boolean | 参数3   |
| ...    | Object  | 参数... |

**请求示例:**

```
{
  "param1": "",
  "param2": "",
  "param3": false,
  "...": ...
}
```

> 响应

**Headers:**

| name         | value                          | required | desc |
|--------------|--------------------------------|----------|------|
| content-type | application/json;charset=UTF-8 | NO       |      |

**Body:**

| name                                      | type    | desc    |
|-------------------------------------------|---------|---------|
| code                                      | string  |         |
| msg                                       | string  |         |
| data                                      | object  |         |
| &ensp;&ensp;&#124;─user                   | object  | 用户信息    |
| &ensp;&ensp;&ensp;&ensp;&#124;─userId     | string  | 第三方用户标识 |
| &ensp;&ensp;&ensp;&ensp;&#124;─userName   | string  | 登录名     |
| &ensp;&ensp;&ensp;&ensp;&#124;─customerNo | string  | 客户号     |
| &ensp;&ensp;&#124;─accessToken            | string  | token   |
| success                                   | boolean |         |

**响应示例:**

```json
{
  "code": "",
  "msg": "",
  "data": {
    "user": {
      "userId": "",
      "userName": "",
      "customerNo": ""
    },
    "accessToken": ""
  },
  "success": false
}
```
