=====================
Get Page Description
=====================

----------------------------------------
POST /get-page-description?page=insights
----------------------------------------
Get page description

**Example Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-page-description?page=insights"

    payload={}
    headers = {}

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)

:Header:

:Params:
        insights

:Example Response:

.. code:: json

    {
        "success": "success",
        "body": {
            "description": "All insights are present here."
        }
    }