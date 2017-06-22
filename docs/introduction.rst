介绍
============

规范
-------------

时丰API使用REST API接口.

除了GET外, 所有端点接受HTTP JSON格式变数, 并会以JSON格式反馈.

所有操作使用标准HTTP动词(GET, POST, PATCH, PUT, DELETE)所有响应使用HTTP状态代码.

动词例子::

    GET /orders/MTK00000001            # 取得订单资料
    POST /orders                       # 建立订单
    PUT /orders/MTK00000001            # 置换订单
    PATCH /orders/MTK00000001          # 更新订单
    DELETE /orders/MTK00000001         # 移除订单

* 以上只作为例子参考, 部份API端点并未开放

通用状态代码::

    200 - 成功 / 请求成功, 详情请检查响应内容
    201 - 建立 / 订单建立
    401 - 未授权 / 金钥为空或错误
    403 - 禁止 / 未有权限进行操作
    404 - 未找到 / 找不到订单
    409 - 冲突 / 找不到订单
    412 - 前提条件失败 / 参数无效, 详情请检查响应内容
    428 - 要求前提条件 / 缺少参数, 详情请检查响应内容

* 状态代码详细解释, 请参考 http://www.restapitutorial.com/httpstatuscodes.html

* 在此的所有关键词（"必须", "不得", "应该", "不应该", "推荐", "可能"和"可选") 遵循文件RFC2119建议 (https://wenku.baidu.com/view/036f0da6f524ccbff1218472.html).

客户端实现
---------------------
此API是与编程语言无关的.

此文档内会提供PHP及Java示例代码.

所有能正确处理HTTP授权及HTTP动词的客户端/代码库均能使用.

示例代码中使用到的代码库:

* PHP: Guzzle - http://guzzlephp.org/
* Java: Okhttp - http://square.github.io/okhttp/
* Java: org.json - https://mvnrepository.com/artifact/org.json/json
