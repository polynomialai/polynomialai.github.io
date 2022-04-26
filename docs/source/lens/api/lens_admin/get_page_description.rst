Get Page Ddescription
=====================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "http://localhost:8000/get-page-description?page=insights"

    payload={}
    headers = {}

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'GET',
    'url': 'http://localhost:8000/get-page-description?page=insights',
    'headers': {
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
            "description": "All insights are present here."
        }
    }