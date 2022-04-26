Get Company Details
===================

**Code snippet for Python Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/get-company-details"

    payload = json.dumps({
    "email": "abcd@gmail.com"
    })
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'POST',
    'url': 'lensservice.polynomial.ai/get-company-details',
    'headers': {
        'apikey': '{{apiKey}}',
        'Content-Type': 'application/json'
    },
    body: JSON.stringify({
        "email": "abcd@gmail.com"
    })

    };
    request(options, function (error, response) {
    if (error) throw new Error(error);
    console.log(response.body);
    });

*Example Response*

.. code:: json

    {
        "status": "success",
        "body": {
            "companyName": "Polynomial.Ai",
            "companyLogo": "https://dummyimage.com/600x400/945494/fff.jpg&text=PA"
        }
    }