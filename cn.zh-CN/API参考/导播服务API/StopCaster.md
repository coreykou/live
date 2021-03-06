# StopCaster {#reference642 .reference}

停止导播台，停止PVW、PGM场景，清理输出配置，停止底层音视频处理任务。

## 请求参数 {#section_k4f_qm1_dfb .section}

|参数|类型|是否必选|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：StopCaster|
|CasterId|String|是|导播台Id|

## 返回参数 {#section_p4f_qm1_dfb .section}

|名称|类型|描述|
|:-|:-|:-|
|RequestId|String|该条任务请求Id|

## 示例 {#section_zcx_4j1_dfb .section}

请求示例

```
https://live.aliyuncs.com?Action=StopCaster&CasterId=80787064-1c94-4dc1-85ce-9409960a9bf0&<公共请求参数> 
```

返回示例

```
{
    "RequestId": "16A96B9A-F203-4EC5-8E43-CB92E68F4CD8"
}
```

## 特殊错误码 {#section_w32_ln3_dfb .section}

|错误代码|描述|Http 状态码|语义|
|:---|:-|:-------|:-|
|PermissionDenied|Permission Denied|401|无权访问导播台|
|InvalidCaster.NotFound|Caster is not found.|404|指定导播台不存在|
|InvalidConfiguration.NotFound|DomainName is not configured|404|配置信息缺失|
|InternalError|InternalError|500|内部错误|

