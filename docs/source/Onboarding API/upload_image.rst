Upload Image
======================

**POST upload**

Example Request:

.. code:: python

    import requests

    url = "https://lensservice.polynomial.ai/upload"

    payload={}
    files=[
    ('file',('day36-abacus.png',open('/home/himanshu/Pictures/forFun/animated/png/day36-abacus.png','rb'),'image/png'))
    ]
    headers = {
    'apikey': '{{apiKey}}'
    }

    response = requests.request("POST", url, headers=headers, data=payload, files=files)

    print(response.text)