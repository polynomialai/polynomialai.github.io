==================================
Add and Update Data Relationship
==================================
------------------------------------
POST /agents/add-edit-data-relation
------------------------------------
Update Data relationship for agent

**Example Request**

.. code::python

    import requests
    import json

    url = "lensservice.polynomial.ai/agents/add-edit-data-relation"

    payload = json.dumps({
      "dataRelation": [
        {
          "brainID": "6180bc63c7dd291d592f3917",
          "columnName": "Column 1"
        }
      ],
      "agentID": "6180bae8d7ba18b5e895b4c8"
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
        "dataRelation":[
            {
            "brainID": "6180bc63c7dd291d592f3917",
            "columnName": "Column 1"
        },{
            "brainID": "6180bc63c7dd291d592f3917",
            "columnName": "Column 2"
        }
        ],
        "agentID": "6194a76fadf9f5001fcb9f79"
    }
