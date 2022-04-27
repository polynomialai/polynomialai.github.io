==================================
Add Update Agent
==================================
--------------------------------
POST /agents/add-update-agent
--------------------------------
Add and Update Agent 

**Example Request**

.. code::python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/add-update-agent"

    payload = json.dumps({
      "kitID": "6180bdcfc7dd291d592f391b",
      "name": "Agent Three",
      "teamID": "6180b85bd7ba18b5e895b4c6",
      "description": "Lorem Ipsum dosem polis menaq senopis filio pinosis blasic misinopa sinopos monolaris",
      "agentID": "6194e084b9d4e0d4c6672d92",
      "imageURL": "",
      "isActive": True
    })
    headers = {
      'apikey': '{{apiKey}}',
      'Content-Type': 'application/json'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)

:Headers:     
      apikey

:Request Body:

.. code:: json

    {
        "kitID": "6180bda7c7dd291d592f3919",
        "name": "Agent One",
        "teamID": "6194e500b83d88df9b7cc377",
        "description": "This agent is for polynomial use only!",
        "agentID": "61b58f0efa6985ba7e1ddae3",
        "imageURL": "",
        "isActive": true
    }
