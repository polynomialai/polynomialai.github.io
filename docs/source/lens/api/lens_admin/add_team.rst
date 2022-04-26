Add Team
========

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/add-team"

    payload = {
                "name": "Team 2",
                "users": ["himanshu.t@polynomial.ai"]
            }
    headers = {
    'apikey': '{{apiKey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var options = {
    'method': 'GET',
    'url': 'lensservice.polynomial.ai/add-team',
    'headers': {
        'apikey': '{{apiKey}}'
    }
    body : {
                "name": "Team 2",
                "users": ["himanshu.t@polynomial.ai"]
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
                    "name": "Team 1",
                    "id": "643839"
                },
                {
                    "name": "Team 2",
                    "id": "643831"
                },
                {
                    "name": "Team 3",
                    "id": "643833"
                },
                {
                    "name": "Team 4",
                    "id": "643834"
                }
            ]
        }
    }   