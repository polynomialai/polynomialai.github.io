==================================
Agent Brain Selected
==================================
--------------------------------------
GET /agents/get-agent-brains-selected
--------------------------------------

Retrieve a list of brains selected for an agent

Example Request:

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/get-agent-brains-selected?agentID=6180bae8d7ba18b5e895b4c8"

    payload = json.dumps({
      "agentID": "6180bae8d7ba18b5e895b4c8"
    })
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

