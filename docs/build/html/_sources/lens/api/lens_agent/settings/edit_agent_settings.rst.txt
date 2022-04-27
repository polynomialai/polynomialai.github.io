==================================
Edit Agent Settings
==================================
--------------------------------
POST /agents/edit-agent-settings
--------------------------------
Update Agent Settings

**Example Request**

.. code::python

    import json

    url = "lensservice.polynomial.ai/agents/edit-agent-settings"

    payload = json.dumps({
      "id": "6180bae8d7ba18b5e895b4c8",
      "agentName": "Agent 1",
      "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
      "imageURL": "",
      "isActive": True,
      "teamID": "6180b85bd7ba18b5e895b4c6"
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
        "id": "6180bae8d7ba18b5e895b4c8",
        "agentName": "Agent 1",
        "description": "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.",
        "imageURL": "",
        "isActive": true,
        "teamID": "6180b85bd7ba18b5e895b4c6"   
    }
