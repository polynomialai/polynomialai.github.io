==================================
Add and Update Insight
==================================
--------------------------------
POST /agents/add-edit-insights
--------------------------------
Update list of insights

**Example Request**

.. code::python

    import requests
    import json

    url = "http://localhost:8000/agents/add-edit-insights"

    payload = json.dumps({
      "insightsId": [
        "1234",
        "4321"
      ],
      "agentId": "43121"
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
    "insightsID":["6180bd4dc7dd291d592f3918"],
    "agentID": "6180bae8d7ba18b5e895b4c8"
}