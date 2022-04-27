=======
Approve
=======

--------------------------------
POST /approve
--------------------------------
Approve user

**Example Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/approve"

    payload = {
        "email": "abc@email.com",
        "quota": 100,
        "role":"user"
    }
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
        "email": "abc@email.com",
        "quota": 100,
        "role":"user"
    }


    