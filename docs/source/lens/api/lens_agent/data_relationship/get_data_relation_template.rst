==================================
Data Relationship Template
==================================
---------------------------------------
GET /agents/get-data-relation-template
---------------------------------------

Retrieve Data Relationship Template for agent

Example Request:

.. code:: python

    import requests
    import json
    
    url = "lensservice.polynomial.ai/agents/get-data-relation-template?agentID=61b5efa89ef90206c8541bba"
    
    payload = ""
    headers = {
      'apikey': '{{apiKey}}',
      'Content-Type': 'application/json'
    }
    
    response = requests.request("GET", url, headers=headers, data=payload)
    
    print(response.text)
        
:Headers:     
      apikey

:Params:
      agentID



