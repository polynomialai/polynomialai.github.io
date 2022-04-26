Get User History
==================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-user-history"

    payload = {"email": "abc@email.com"}
    headers = {
    'apikey': '{{apiKey}}'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'POST',
    'url': 'lensservice.polynomial.ai/get-user-history',
    'headers': {
        'apikey': '{{apiKey}}'
    },
    body: {"email": "abc@email.com"}

    };
    request(options, function (error, response) {
    if (error) throw new Error(error);
    console.log(response.body);
    });


    