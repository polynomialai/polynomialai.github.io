==================================
Get Agent Info
==================================
-----------------------------------
GET /agents/get-agents-info
-----------------------------------

Retrieve agent info

Example Request:

.. code:: python

    import requests
    import json
    
    url = "lensservice.polynomial.ai/agents/get-agent-info?agentID=6180bae8d7ba18b5e895b4c8"
    
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
