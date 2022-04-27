==================================
Get Account Detail
==================================
--------------------------------
GET /get-account
--------------------------------

Example Request:

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-account"

    payload={}
    headers = {
    'apikey': '{{apikey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


:Headers: 
    apikey

:Params: 

:Request Body:

:Example Response