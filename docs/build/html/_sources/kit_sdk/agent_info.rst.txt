Agent Info
===================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/kit/analytics"

    payload = ""
    headers = {
    'accesskey': 'U2FsdGVkX1/khcNwmjLsSOTrzmAebBtdbfsmXHhN3IRoBIKwb4ZKtkNiTNwXqaXf0tE90qCUNAyLSSclX7v1ipjNOW7lTAvomaR5Yh0KlEzwjrJsxuOLbVGR/uf0AtZ9h0mXQTbwzqpTw2Ed9Qcr+exVLMVpaAAbwn4zTc80Z17WEocBbSLvwS5oggVd0Jeh+ecUXxseS4bj+hR2wEqVgc24nGatQaPVExOXML0FsJzpgaqpiXrsGVfayoRRSeW6riyqM/hyy6CbG6FgtYExWcvLRSht1Odu1z+b9p//kIbawnoCUSeo8vO/XmBouhp64UqTehp8x7YiyVxx/38B5XBJxqWi8nVE+SSDZzKB4vI0D2iP/In1gqUcV5gf7nksHmCG0Vt+ESY9FUhEOZ0QYA==',
    'agentID': '61b5efa89ef90206c8541bba'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


**Sample Response Json**

.. code:: json

    {
      "success": "success",
      "body": {
        "totalUptime": 14140726976,
        "totalRequests": 59,
        "avgResponseTime": 51659,
        "totalInsightServed": 246,
        "quotaRemaining": 9270
      }
    }