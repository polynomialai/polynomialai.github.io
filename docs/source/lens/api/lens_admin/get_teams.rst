Get Teams
=========

**Code snippet for Python Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/get-teams"

    payload = ""
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'GET',
    'url': 'lensservice.polynomial.ai/get-teams',
    'headers': {
        'apikey': '{{apiKey}}',
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
            "teams": [
            {
                "_id": "6180b85bd7ba18b5e895b4c6",
                "name": "Team 1",
                "users": [
                "6077e794ce8111001ee31779",
                "60cc9067e434b10030e89281",
                "6086b1a5fe1f42001e8d5a31"
                ],
                "createdAt": "2021-11-02T04:04:25.619Z"
            }
                ]
        }
    }