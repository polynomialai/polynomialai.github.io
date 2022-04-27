Get Profile
=================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/get-profile"

    payload={}
    headers = {
    'apikey': '{{apikey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)