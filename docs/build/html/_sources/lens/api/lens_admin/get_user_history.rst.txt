==================
Get User History
==================

--------------------------------
POST /get-user-history
--------------------------------
Get user history

**Example Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-user-history"

    payload = {"email": "abc@email.com"}
    headers = {
    'apikey': '{{apiKey}}'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


:Headers:     
      apikey
    
:Params:

:Request Body:

.. code:: json
    
    {
        "email": "abc@email.com"
    }


    