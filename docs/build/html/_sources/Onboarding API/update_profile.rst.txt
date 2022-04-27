update profile
===================

**POST update-profile**

Example Request:

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/update-profile"

    payload = json.dumps({
    "userName": "Swapnil Kapad",
    "displayPicture": "https://polynomialservices.blob.core.windows.net/stores/WmiKSCBWzrEd_RZQrwPGlnqc.jpg"
    })
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)