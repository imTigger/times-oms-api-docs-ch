介绍
============

规范
-------------

时丰API使用REST API接口.

除了GET外, 所有接口接受HTTP JSON格式变数, 并会以JSON格式反馈.

所有操作使用标准HTTP动词(GET, POST, PATCH, PUT, DELETE)所有响应使用HTTP状态代码.

动词例子::

    GET /orders/MTK00000001            # 取得订单资料
    POST /orders                       # 建立订单
    PUT /orders/MTK00000001            # 置换订单
    PATCH /orders/MTK00000001          # 更新订单
    DELETE /orders/MTK00000001         # 移除订单

* 以上只作为例子参考, 部份API接口并未开放

通用状态代码::

    200 - 成功 / 请求成功, 详情请检查响应内容
    201 - 建立 / 订单建立
    401 - 未授权 / 金钥为空或错误
    403 - 禁止 / 未有权限进行操作
    404 - 未找到 / 找不到订单
    409 - 冲突 / 找不到订单
    412 - 前提条件失败 / 参数无效, 详情请检查响应内容
    428 - 要求前提条件 / 缺少参数, 详情请检查响应内容

* For detailed status code explanations, please refer to http://www.restapitutorial.com/httpstatuscodes.html

* All Key words ("MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL") in this document follows RFC2119 recommandations (https://tools.ietf.org/html/rfc2119).

Client Implementation
---------------------
The API is language independent.

While this document provides PHP and Java sample code.

Any client/library that can correctly handle `Authorization` HTTP header and HTTP verbs can be used.

Libraries used in sample code:

* PHP: Guzzle - http://guzzlephp.org/
* Java: Okhttp - http://square.github.io/okhttp/
