# 创建客户VPN网关 - CreateRemoteVPNGateway

## 简介

创建客户VPN网关






## 使用方法

您可以选择以下方式中的任意一种，发起 API 请求：
- 多语言 OpenSDK / [Go](https://github.com/ucloud/ucloud-sdk-go) / [Python](https://github.com/ucloud/ucloud-sdk-python3) /
- [UAPI 浏览器](https://console.ucloud.cn/uapi/detail?id=CreateRemoteVPNGateway)
- [CloudShell 云命令行](https://shell.ucloud.cn/)


## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `CreateRemoteVPNGateway`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Region** | string | 地域。 参见 [地域和可用区列表](api/summary/regionlist) |**Yes**|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](api/summary/get_project_list) |**Yes**|
| **RemoteVPNGatewayName** | string | 客户VPN网关名称 |**Yes**|
| **RemoteVPNGatewayAddr** | string | 客户VPN网关地址 |**Yes**|
| **Tag** | string | 业务组名称，默认为 "Default" |No|
| **Remark** | string | 备注，默认为空 |No|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **RemoteVPNGatewayId** | string | 新建客户VPN网关的资源ID |No|




## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=CreateRemoteVPNGateway
&Region=cn-sh2
&ProjectId=org-XXXXXX
&RemoteVPNGatewayName=test
&RemoteVPNGatewayAddr=1.1.1.1
&Tag=test
&Remark=test
```

### 响应示例
    
```json
{
  "Action": "CreateRemoteVPNGatewayResponse",
  "RemoteVPNGatewayId": "remotevpngw-XXXXX",
  "RetCode": 0
}
```





