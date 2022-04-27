==================================
Update Account Detail
==================================
--------------------------------
POST /update-account
--------------------------------

Example Request:

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/update-account"

    payload = json.dumps({
    "language": "English",
    "isDesktopNotificationAllowed": False,
    "isEmailNotificationAllowed": False,
    "plan": "Basic Plan"
    })
    headers = {
    'apikey': '{{apiKey}}',
    'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)

:Headers: 
    apiKey
    
:Params: 

:Request Body:
    .. code:: json
        
        {
            "language": "English",
            "isDesktopNotificationAllowed": false,
            "isEmailNotificationAllowed": false,
            "plan": "Basic Plan"
        }

:Example Response