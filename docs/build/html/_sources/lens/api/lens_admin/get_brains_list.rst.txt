===============
Get Brains List
===============

--------------------------------
POST /agents/get-brains-list
--------------------------------
Get all brains

**Example Request**

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

:Headers:     
      apikey
    
:Params:


:Example Response:

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