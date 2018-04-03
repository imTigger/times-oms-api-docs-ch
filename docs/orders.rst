订单
======

建立订单
----------

建立订单(没有当地派送编号) [POST /orders]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Postman Collections: https://www.getpostman.com/collections/3120f45724992dcc5913

+ 参数
    + consigneeCompanyName: (字串, 可选) - 收货人公司(英语)
    + consigneeContactName: (字串, 可选) - 收货人联络人(英语)
    + consigneePhone: (字串, 必须) - 收货人电话
    + consigneeAddress: (字串, 可选) - 收货人地址(英语)
    + consigneeSubdistrict: (字串, 必须) - 收货人分区份
    + consigneeDistrict: (字串, 必须) - 收货人区份
    + consigneeProvince: (字串, 必须) - 收货人省份
    + consigneeCountry: (字串, 必须) - 收货人国家(英语)
    + consigneeCompanyNameLocale: (字串, 可选) - 收货人公司(目的地官方语言)
    + consigneeContactNameLocale: (字串, 必须) - 收货人联络人(目的地官方语言)
    + consigneeIdCardNumber: (字串, 可选/必须) - 收货人身份证编号. 如目的地为中国台湾, 总货价大或等於3000当地货币必须
    + consigneeAddressLocale: (字串, 必须) - 收货人地址(目的地官方语言)
    + consigneePostalCode: (字串, 必须) - 收货人邮政编号
    + shipperCompanyName: (字串, 必须) - 发货人公司(英语)
    + shipperContactName: (字串, 必须) - 发货人联络人(英语)
    + shipperPhone: (字串, 必须) - 发货人电话
    + shipperAddress: (字串, 必须) - 发货人地址(英语)
    + shipperSubdistrict: (字串, 必须) - 发货人分区份(英语)
    + shipperDistrict: (字串, 必须) - 发货人区份(英语)
    + shipperProvince: (字串, 必须) - 发货人省份(英语)
    + shipperCountry: (字串, 必须) - 发货人国家(英语)
    + shipperPostalCode: (字串, 必须) - 发货人邮政编号
    + paymentMethod: (字串, 必须) - 付款方式
    + productType: (字串, 可选) - 寄货渠道: Express = 专线; Postal = 邮政
    + shipmentType: (整数, 可选) - 包裹类型: General Shipment = 普货; Sensitive Shipment = 带电池货(敏感货); Mobile & Tablet = 手机及平板计算机
    + salePlatformName: (字串, 必须) - 销售平台名称
    + referenceNumber: (字串, 必须) - 客户参考编号, 客戶对包裹的唯一识别号
    + items[]: (阵列, 必须) - 货品内容阵列
    + items[][sku]: (字串, 可选/必须) - 货品SKU
    + items[][categoryId]: (字串, 必须) - 货品分类编号
    + items[][categoryName]: (字串, 必须) - 货品分类名称
    + items[][description]: (字串, 必须) - 品名
    + items[][specification]: (字串, 可选) - 规格
    + items[][descriptionOriginal]: (字串, 可选) - 起步港语言品名, 如与目的港语言相同则不用填写
    + items[][specificationOriginal]: (字串, 可选) - 起步港语言规格, 如与目的港语言相同则不用填写
    + items[][brand]: (字串, 可选/必须) - 牌子. 如包裹类型为手机及平板计算机, 此项必填
    + items[][model]: (字串, 可选/必须) - 型号. 如包裹类型为手机及平板计算机, 此项必填
    + items[][pieces]: (整数, 必须) - 单项SKU件数
    + items[][unitPrice]: (十进制数, 必须) - 单项SKU单价
    + items[][unitPriceCurrency]: (字串, 必须) - 货币单位, 使用ISO 4217标准
    + items[][CODValue]: (十进制数, 可选/必须) - 单项SKU COD货价(件数*COD单价). 如付款方式为COD, 此项必填. 使用当地货币

建立订单(已有当地派送编号) [POST /orders/{trackingNumber}]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Postman Collection: https://www.getpostman.com/collections/9f944b3d95d1324237d0

+ 参数
    + consigneeCompanyName: (字串, 可选) - 收货人公司(英语)
    + consigneeContactName: (字串, 可选) - 收货人联络人(英语)
    + consigneePhone: (字串, 必须) - 收货人电话
    + consigneeAddress: (字串, 可选) - 收货人地址(英语)
    + consigneeSubdistrict: (字串, 必须) - 收货人分区份
    + consigneeDistrict: (字串, 必须) - 收货人区份
    + consigneeProvince: (字串, 必须) - 收货人省份
    + consigneeCountry: (字串, 必须) - 收货人国家(英语)
    + consigneeCompanyNameLocale: (字串, 可选) - 收货人公司(目的地官方语言)
    + consigneeContactNameLocale: (字串, 必须) - 收货人联络人(目的地官方语言)
    + consigneeIdCardNumber: (字串, 可选/必须) - 收货人身份证编号. 如目的地为中国台湾, 总货价大或等於3000当地货币必须
    + consigneeAddressLocale: (字串, 必须) - 收货人地址(目的地官方语言)
    + consigneePostalCode: (字串, 必须) - 收货人邮政编号
    + shipperCompanyName: (字串, 必须) - 发货人公司(英语)
    + shipperContactName: (字串, 必须) - 发货人联络人(英语)
    + shipperPhone: (字串, 必须) - 发货人电话
    + shipperAddress: (字串, 必须) - 发货人地址(英语)
    + shipperSubdistrict: (字串, 必须) - 发货人分区份(英语)
    + shipperDistrict: (字串, 必须) - 发货人区份(英语)
    + shipperProvince: (字串, 必须) - 发货人省份(英语)
    + shipperCountry: (字串, 必须) - 发货人国家(英语)
    + shipperPostalCode: (字串, 必须) - 发货人邮政编号
    + paymentMethod: (字串, 必须) - 付款方式
    + productType: (字串, 可选) - 寄货渠道: Express = 专线; Postal = 邮政
    + shipmentType: (整数, 可选) - 包裹类型: General Shipment = 普货; Sensitive Shipment = 带电池货(敏感货); Mobile & Tablet = 手机及平板计算机
    + salePlatformName: (字串, 必须) - 销售平台名称
    + referenceNumber: (字串, 必须) - 客户参考编号, 客戶对包裹的唯一识别号
    + items[]: (阵列, 必须) - 货品内容阵列
    + items[][sku]: (字串, 可选/必须) - 货品SKU
    + items[][categoryId]: (字串, 必须) - 货品分类编号
    + items[][categoryName]: (字串, 必须) - 货品分类名称
    + items[][description]: (字串, 必须) - 品名
    + items[][specification]: (字串, 可选) - 规格
    + items[][descriptionOriginal]: (字串, 可选) - 起步港语言品名, 如与目的港语言相同则不用填写
    + items[][specificationOriginal]: (字串, 可选) - 起步港语言规格, 如与目的港语言相同则不用填写
    + items[][brand]: (字串, 可选/必须) - 牌子. 如包裹类型为手机及平板计算机, 此项必填
    + items[][model]: (字串, 可选/必须) - 型号. 如包裹类型为手机及平板计算机, 此项必填
    + items[][pieces]: (整数, 必须) - 单项SKU件数
    + items[][unitPrice]: (十进制数, 必须) - 单项SKU单价
    + items[][unitPriceCurrency]: (字串, 必须) - 货币单位, 使用ISO 4217标准
    + items[][CODValue]: (十进制数, 可选/必须) - 单项SKU COD货价(件数*COD单价). 如付款方式为COD, 此项必填. 使用当地货币

请求 (application/json)
^^^^^^^^^^^^^^^^^^^^^^^^^

消息主体 (示例)
""""""""""""""""

.. code-block:: json

      {
        "consigneeCompanyName": "Supachai Piamthong",
        "consigneeContactName": "Supachai Piamthong",
        "consigneePhone": "123456789",
        "consigneeAddress": "12 34 Moo 8 Chom Bueng Ratchaburi Ratchaburi Chom Bueng 70150",
        "consigneeSubdistrict":"ท่ายาง",
        "consigneeDistrict":"เมืองพิษณุโลก",
        "consigneeProvince":"Bangkok",
        "consigneeCountry": "Thailand",
        "consigneePostalCode": "70150",
        "consigneeCompanyNameLocale": "\u0e28\u0e38\u0e20\u0e0a\u0e31\u0e22  \u0e40\u0e1b\u0e35\u0e48\u0e22\u0e21\u0e17\u0e2d\u0e07",
        "consigneeContactNameLocale": "\u0e28\u0e38\u0e20\u0e0a\u0e31\u0e22  \u0e40\u0e1b\u0e35\u0e48\u0e22\u0e21\u0e17\u0e2d\u0e07",
        "consigneeAddressLocale": "90 100 \u0e21 8 \u0e15 \u0e08\u0e2d\u0e21\u0e1a\u0e36\u0e07  \u0e23\u0e32\u0e0a\u0e1a\u0e38\u0e23\u0e35  Ratchaburi \u0e08\u0e2d\u0e21\u0e1a\u0e36\u0e07  Chom Bueng 70150",
        "shipperCompanyName": "ABC",
        "shipperContactName": "DEF",
        "shipperPhone": "(501) 123-4567",
        "shipperAddress": "Room 1, HaoQuan Building, 1st Jichangdongmen Road Jingtai Street, Baiyun District, Guangzhou province, China",
        "shipperSubdistrict":"Baoan",
        "shipperDistrict":"Shenzheng",
        "shipperProvince":"Guangdong",
        "shipperCountry": "China",
        "shipperPostalCode": "000000",
        "paymentMethod": "COD",
        "productType": "Express",
        "shipmentType": "Mobile & Tablet",
        "salePlatformName": "Amazon",
        "referenceNumber": "PTK0000156852",
        "items": [
            {
                 "sku": "sku-test-1234567890",
                 "categoryId": "ASQW987654",
                 "categoryName": "Mobile",
                 "description": "Apple new iphone 7 red 128g unlocked",
                 "brand": "Apple",
                 "model": "iphone 7",
                 "pieces": "2",
                 "unitPrice": "387",
                 "unitPriceCurrency": "THB",
                 "CODValue": "774"
            },
            {
                 "sku": "sku-test-9876543210",
                 "categoryId": "WERT987654",
                 "categoryName": "Mobile",
                 "description": "Xiaomu note 3 64gb",
                 "brand": "XiaoMu",
                 "model": "note 3",
                 "pieces": "1",
                 "unitPrice": "856",
                 "unitPriceCurrency": "THB",
                 "CODValue": "856"
            }
        ]
      }


响应 201 (application/json)
"""""""""""""""""""""""""""""

.. code-block:: json

            {
                "message": "Success",
                "trackingNumber": "TN123456789",
                "sortCode": "SC1234"
            }


响应 409 (application/json)
"""""""""""""""""""""""""""""""

.. code-block:: json

            {
                "message": "Order already exist",
                "status_code": 409,
                "remarks": {
                    "trackingNumber": "TN123456789",
                    "sortCode": "SC1234"
                }
            }

响应 412 (application/json)
"""""""""""""""""""""""""""""""

.. code-block:: json

            {
                "message": "Order already exist or invalid parameter",
                "status_code": 412,
                "remarks": {
                    "trackingNumber": "TN123456789",
                    "sortCode": "SC1234"
                }
            }

响应 428 (application/json)
"""""""""""""""""""""""""""""""

.. code-block:: json

            {
                "message": "Missing parameter",
                "status_code": 428
            }

取得订单资料
--------------

取得订单资料 [GET /orders/{trackingNumber}]
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

响应 200 (application/json)
""""""""""""""""""""""""""""""

.. code-block:: json

            {
                "trackingNumber": "MTK00000001",
                "milestones": {
                    "upload": "2017-01-01 00:00:00",
                    "inbound": "2017-01-01 01:00:00",
                    "outbound": "2017-01-01 02:00:00",
                    "close_box": "2017-01-01 03:00:00",
                    "handover_linehaul": null,
                    "pickup": null,
                    "export": null,
                    "uplift": null,
                    "import": null,
                    "handover_lastmile": null,
                    "delivering": null,
                    "pending": null,
                    "pending_reason": null,
                    "reject": null,
                    "reject_reason": null,
                    "return": null,
                    "receive": null
                }
            }

响应 404 (application/json)
"""""""""""""""""""""""""""""""

.. code-block:: json

            {
                "message": "Order not found",
                "status_code": 404
            }
