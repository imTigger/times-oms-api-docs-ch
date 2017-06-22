API 端点 及 API 钩子触发
==========================

API 端点
-------------

API 端点需要由您的服务器发送请求到时丰OMS的服务器, 用以搜寻, 建立, 更新或移除资料.

必须先提供身份验证才能调用API端点调用.

API 钩子触发
------------

API Webhooks are automated calls from TEC servers to your server triggered when a specific event happened.

For example, an order status update and you want to know about it in real time.

You MAY register a webhook url in our system, so we can make a HTTP POST requests to "push" data to your server.

You SHOULD verify the HTTP requests before performing any actions with the data received.

While we support both HTTP/HTTPS urls for webhook, HTTPS is RECOMMENDED for better security.
