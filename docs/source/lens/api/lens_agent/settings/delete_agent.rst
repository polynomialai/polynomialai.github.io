==================================
Delete Agent 
==================================
--------------------------------
DEL /agents/delete-agent
--------------------------------
Update Agent Settings

**Example Request**

.. code::python

    import requests
    import json

    url = "http://localhost:8000/agents/delete-agent"

    payload = json.dumps({
      "id": "321312"
    })
    headers = {
      'apikey': '{{apikey}}',
      'Content-Type': 'application/json'
    }

    response = requests.request("DELETE", url, headers=headers, data=payload)

    print(response.text)

:Headers:     
      apikey

:Request Body:
      agentID
