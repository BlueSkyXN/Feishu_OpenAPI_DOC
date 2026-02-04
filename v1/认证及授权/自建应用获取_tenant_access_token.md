# 自建应用获取 tenant\_access\_token

最后更新于 2025-03-26

自建应用通过此接口获取 `tenant_access_token`。

## 注意事项

`tenant_access_token` 的最大有效期是 2 小时。

* 剩余有效期小于 30 分钟时，调用本接口会返回一个新的 `tenant_access_token`，这会同时存在两个有效的 `tenant_access_token`。
* 剩余有效期大于等于 30 分钟时，调用本接口会返回原有的 `tenant_access_token`。

## 请求

| 基本           |                                                                         |
| ---------------- | ------------------------------------------------------------------------- |
| HTTP URL       | https://open.feishu.cn/open-apis/auth/v3/tenant\_access\_token/internal |
| HTTP Method    | POST                                                                    |
| 支持的应用类型 | **仅自建应用**                                                          |
| 权限要求       | 无                                                                      |

### 请求头

| 名称         | 类型   | 必填 | 描述                                                    |
| -------------- | -------- | ------ | --------------------------------------------------------- |
| Content-Type | string | 是   | ​**固定值**​："application/json; charset=utf-8" |

### 请求体

| 名称            | 类型       | 必填 | 描述                                                                                                                                                                                                 |
| ----------------- | ------------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **app\_id**     | **string** | 是   | 应用唯一标识，创建应用后获得。有关`app_id` 的详细介绍。请参考[通用参数](https://open.feishu.cn/document/ukTMukTMukTM/uYTM5UjL2ETO14iNxkTN/terminology)介绍**示例值：** "cli\_slkdjalasdkjasd" |
| **app\_secret** | **string** | 是   | 应用秘钥，创建应用后获得。有关 `app_secret` 的详细介绍，请参考[通用参数](https://open.feishu.cn/document/ukTMukTMukTM/uYTM5UjL2ETO14iNxkTN/terminology)介绍**示例值：** "dskLLdkasdjlasdKK"   |

### 请求体示例

```
{    "app_id": "cli_slkdjalasdkjasd",    "app_secret": "dskLLdkasdjlasdKK"}
```

## 响应

### 响应体

| 名称                      | 类型       | 描述                                           |
| --------------------------- | ------------ | ------------------------------------------------ |
| **code**                  | **int**    | 错误码，非 0 取值表示失败                      |
| **msg**                   | **string** | 错误描述                                       |
| **tenant\_access\_token** | **string** | 租户访问凭证                                   |
| **expire**                | **int**    | `tenant_access_token` 的过期时间，单位为秒 |

### 响应体示例

```
{    "code": 0,    "msg": "ok",    "tenant_access_token": "t-caecc734c2e3328a62489fe0648c4b98779515d3",    "expire": 7200}
```
