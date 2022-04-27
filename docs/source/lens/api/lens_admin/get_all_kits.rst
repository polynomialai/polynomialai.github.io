========
All Kits
========
--------------------------------
POST /kit/get-all-kits
--------------------------------
Get all Kits

**Example Request**

.. code:: python

    import requests
    import json

    url = "http://lensservice.polynomial.ai/kit/get-all-kits"

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
        "kits": [
        {
            "_id": "6180b9e4c7dd291d592f3916",
            "name": "Meeting Kit",
            "description": "Lorem Ipsum is a simple dummy text for display.",
            "version": "v1",
            "imageURL": "",
            "createdAt": "2021-11-02T04:04:25.619Z"
        },
        {
            "_id": "6180bda7c7dd291d592f3919",
            "name": "Review Kit",
            "description": "Lorem Ipsum is a simple dummy text for display.",
            "version": "v1",
            "imageURL": "",
            "createdAt": "2021-11-02T04:04:25.619Z"
        },
        {
            "_id": "6180bdbdc7dd291d592f391a",
            "name": "Customer Ticket Kit",
            "description": "Lorem Ipsum is a simple dummy text for display.",
            "version": "v1",
            "imageURL": "",
            "createdAt": "2021-11-02T04:04:25.619Z"
        },
        {
            "_id": "6180bdcfc7dd291d592f391b",
            "name": "Normal Text",
            "description": "Lorem Ipsum is a simple dummy text for display.",
            "version": "v1",
            "imageURL": "",
            "createdAt": "2021-11-02T04:04:25.619Z"
        }
        ]
    }
    }