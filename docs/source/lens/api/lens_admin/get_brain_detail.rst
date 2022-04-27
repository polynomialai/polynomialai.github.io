==================
Get Brains Details
==================

--------------------------------
POST /brains/get-all-brains
--------------------------------
Get brains details

**Example Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/brains/get-all-brains"

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
      agentID

:Example Response:

.. code:: json

    {
        "success": "success",
        "body": {
            "brains": [
                {
                    "_id": "6180bc63c7dd291d592f3917",
                    "name": "Emotion and Sentiment",
                    "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                    "subDescription": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
                    "subBrains": [
                    {
                        "name": "Love",
                        "id": "1234"
                    },
                    {
                        "name": "Hate",
                        "id": "1243"
                    },
                    {
                        "name": "Greed",
                        "id": "1324"
                    },
                    {
                        "name": "Optimism",
                        "id": "2134"
                    }
                    ],
                    "imgURL": "",
                    "createdAt": "2021-11-02T04:04:25.619Z"
                }
            ]
        }
    }