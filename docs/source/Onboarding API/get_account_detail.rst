Get Account Detail
===================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-account"

    payload={}
    headers = {
    'apikey': '{{apikey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)