Get Brains List
===============

**Code snippet for Python Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/get-brains-list"

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
    'url': 'lensservice.polynomial.ai/agents/get-brains-list',
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
            "brains": [
                {
                    "_id": "6180bc63c7dd291d592f3917",
                    "name": "Emotion and Sentiment"
                }
            ]
        }
    }