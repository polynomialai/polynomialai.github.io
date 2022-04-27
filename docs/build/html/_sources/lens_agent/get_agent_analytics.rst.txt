==================================
Get All Agents Analytics
==================================
-----------------------------------
GET /agents/get-agents-analytics
-----------------------------------

Retrieve a list of agents analytics

Example Request:

.. code:: python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/get-agent-analytics?filters={ \"brains\":[], \"timeframe\": \"monthly\" }&agentID=61b5efa89ef90206c8541bba"

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

.. code:: json
        [
          {
            "_id": "6180bc63c7dd291d592f3917"
          },
          {
            "_id": "619370a7279636235a1c5c4d"
          }
        ]