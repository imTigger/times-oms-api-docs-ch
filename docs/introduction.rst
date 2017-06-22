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
    PUT /orders/MTK00000001            # Replace an Order
    PATCH /orders/MTK00000001          # Update an Order
    DELETE /orders/MTK00000001         # Delete an Order

* For example only, not all API are implemented

Common Status Code::

    200 - Okay / Query success, please check the response
    201 - Created / Order created
    401 - Unauthorized / Token missing or invalid
    403 - Forbidden / Operation not permited
    404 - Not Found / Order is not found
    409 - Conflict / Order already exist
    412 - Precondition Failed / Invalid parameter, check response message for reason
    428 - Precondition Required / Missing parameter, check response message for reason

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
