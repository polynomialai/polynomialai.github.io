==================================
Whitelisted Domain
==================================
-----------------------------------
GET /agents/get-whitelist-domains
-----------------------------------

Retrieve a list of Whitelisted domain for agent

Example Request:

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/get-whitelist-domains?agentID=6180bae8d7ba18b5e895b4c8"

    payload = ""
    headers = {
      'apikey': '{{apikey}}',
      'Content-Type': 'application/json'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


:Headers:     
      apikey

:Params:
      agentID

--------------------------------
POST /agents/add-update-domains
--------------------------------
Update list of domains

**Example Request**

.. code::python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/add-update-domains"

    payload = json.dumps({
      "whitelistedDomains": [
        "https://google.com",
        "https://facebook.com",
        "https://twitter.com"
      ],
      "agentID": "6180bae8d7ba18b5e895b4c8"
    })
    headers = {
      'apikey': '{{apikey}}',
      'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)

:Headers:     
      apikey

:Request Body:

.. code:: json

    {
        "whitelistedDomains":["https://google.com","https://facebook.com", "https://twitter.com"],
        "agentID": "619295aa20053bc53a703d5e"
    
    }
      