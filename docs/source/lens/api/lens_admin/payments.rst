Payments
========


**Code snippet for Python Request**

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


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'GET',
    'url': 'http://lensservice.polynomial.ai/payment/get-all-plans',
    'headers': {
        'apikey': '{{apikey}}',
        'Content-Type': 'application/json'
    }
    };
    request(options, function (error, response) {
    if (error) throw new Error(error);
    console.log(response.body);
    });

*Example Response*

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