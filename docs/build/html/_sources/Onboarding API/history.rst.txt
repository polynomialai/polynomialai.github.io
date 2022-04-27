History
=================

**POST history**

Example Request:

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/history"

    payload={}
    headers = {
    'apikey': '{{apikey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)