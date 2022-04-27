==================================
Add and Update Domain
==================================
--------------------------------
POST /agents/add-edit-brains
--------------------------------
Update list of brains

**Example Request**

.. code::python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/add-edit-brains"

    payload = json.dumps({
      "brains": [
        {
          "id": "6180bc63c7dd291d592f3917",
          "subBrains": [
            "Love"
          ]
        }
      ],
      "agentID": "6180bae8d7ba18b5e895b4c8"
    })
    headers = {
      'apikey': '{{apikey}}',
      'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)

:Headers:     
      apikey

:Request Body:

.. code:: json
    
    {
        "brains":[
            {
                "id": "61937101279636235a1c5c51",
                "subBrains":[]
            },
            {
                "id": "619370a7279636235a1c5c4d",
                "subBrains":[]
            }
        ],
        "agentID": "61b5efa89ef90206c8541bba"
    }