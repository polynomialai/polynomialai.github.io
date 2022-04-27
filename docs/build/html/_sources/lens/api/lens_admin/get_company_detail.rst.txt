===================
Get Company Details
===================

--------------------------------
POST /get-company-details
--------------------------------
Get company details

**Example Request**

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/get-company-details"

    payload = json.dumps({
    "email": "abcd@gmail.com"
    })
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


:Headers:     
        apikey

:Params:

:Request Body:

.. code:: json
    
    {
        "email": "himanshu.t@polynomial.ai"
    }

:Example Response:

.. code:: json

    {
        "status": "success",
        "body": {
            "companyName": "Polynomial.Ai",
            "companyLogo": "https://dummyimage.com/600x400/945494/fff.jpg&text=PA"
        }
    }