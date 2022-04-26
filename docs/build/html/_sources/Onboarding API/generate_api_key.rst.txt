Generate API Key
=================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/generate-api-key"

    payload = {
                "email": "prakhar.k@polynomial.ai",
                "password": "Prakhar@123"
            }
    headers = {}

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)