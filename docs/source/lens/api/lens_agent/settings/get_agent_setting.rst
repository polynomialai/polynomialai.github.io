==================================
Agent Settings
==================================
-----------------------------------
GET /agents/get-agent-settings
-----------------------------------

Retrieve a list of Agent Settings

Example Request:

.. code:: python

    import requests
    import json
    
    url = "lensservice.polynomial.ai/agents/get-agent-settings?agentID=6180bae8d7ba18b5e895b4c8"
    
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

