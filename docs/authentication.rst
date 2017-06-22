认证
================


规范
-------------

作为REST API, 服务器端不会存储任何状态.

因此必须在每个请求中的HTTP请求头中提供"令牌".

请注意, API使用的"令牌"是不同于钩子触发中使用的"密钥".

获取API令牌
-------------------

API令牌可以在时丰OMS平台中获得, 或会由时丰IT部门提供.

重置API令牌
-------------------

如果您认为您的API令牌已经外泄, 您可以在时丰OMS平台中请求令牌重置.

重置后, 将会发出一个新的令牌, 而旧的令牌亦会立即失效.

令牌有效时间
--------------

除非被重置, 否则令牌永远不会过期.

令牌使用示例
-------------------

使用API令牌 piAOLkaYYBdscIv5YxsrYuiuFH7vwC231YlJ4kivW43iFJMp59blGLJGysKc发送Bare Minimal HTTP请求::

    GET /api/orders/MTK00000001 HTTP/1.1
    Authorization: Bearer piAOLkaYYBdscIv5YxsrYuiuFH7vwC231YlJ4kivW43iFJMp59blGLJGysKc
