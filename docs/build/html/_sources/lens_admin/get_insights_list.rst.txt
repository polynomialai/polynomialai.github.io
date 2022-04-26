Get Insights List
==================

**Code snippet for Python Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/insights/get-insights-list"

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
    'url': 'lensservice.polynomial.ai/insights/get-insights-list',
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
                "insights": [
                {
                    "_id": "6180bd4dc7dd291d592f3918",
                    "title": "Sentiment vs Gender",
                    "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                    "insightVisual": "",
                    "imgURL": "",
                    "createdAt": "2021-11-02T04:04:25.619Z"
                }
            ]
        }
    }