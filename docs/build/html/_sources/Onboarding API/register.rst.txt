Register
========

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/register"

    payload =  {
                "email": "abc@email.com",
                "password": "123456"
                }
    headers = {}

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


