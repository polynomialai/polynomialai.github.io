Change Password
===================

**POST change-password**

Example Request:

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/change-password"

    payload = json.dumps({
    "oldPassword": "Himanshu@123",
    "newPassword": "Himanshu@1234",
    "confirmPassword": "Himanshu@1234"
    })
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)