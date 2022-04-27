=========
Payments
=========

--------------------------------
POST /payment/get-all-plans
--------------------------------
Get all plans

**Example Request**

.. code:: python

    import requests
    import json

    url = "http://lensservice.polynomial.ai/payment/get-all-plans"

    payload = ""
    headers = {
    'apikey': '{{apikey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)

:Headers:     
      apikey

:Params: 

:Example Response:

.. code:: json

    {
    "success": "success",
    "body": {
        "plans": [
        {
            "id": "8999",
            "title": "Standard",
            "price": 30,
            "quirks": [
            "Agent Creation",
            "Add Brains",
            "Insight",
            "Data Relationships",
            "Analytics Dashboard"
            ]
        }
        ]
    }
    }