==================================
Data Relationship
==================================
-----------------------------------
GET /agents/get-data-relation
-----------------------------------

Retrieve Data Relationship for agent

Example Request:

.. code:: python

    import requests
    import json
    
    url = "lensservice.polynomial.ai/agents/get-data-relation?agentID=6180bae8d7ba18b5e895b4c8"
    
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


