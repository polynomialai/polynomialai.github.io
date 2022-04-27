Quota
=================

**Code snippet for Python Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/quota"

    payload={}
    headers = {
    'apikey': '{{apikey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)