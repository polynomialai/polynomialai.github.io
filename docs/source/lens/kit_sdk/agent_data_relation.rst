==================================
Agent Data Relation
==================================
--------------------------------
GET kit/dataRelations
--------------------------------

Example Request:

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/kit/dataRelations"

    payload = ""
    headers = {
    'accesskey': 'U2FsdGVkX1/khcNwmjLsSOTrzmAebBtdbfsmXHhN3IRoBIKwb4ZKtkNiTNwXqaXf0tE90qCUNAyLSSclX7v1ipjNOW7lTAvomaR5Yh0KlEzwjrJsxuOLbVGR/uf0AtZ9h0mXQTbwzqpTw2Ed9Qcr+exVLMVpaAAbwn4zTc80Z17WEocBbSLvwS5oggVd0Jeh+ecUXxseS4bj+hR2wEqVgc24nGatQaPVExOXML0FsJzpgaqpiXrsGVfayoRRSeW6riyqM/hyy6CbG6FgtYExWcvLRSht1Odu1z+b9p//kIbawnoCUSeo8vO/XmBouhp64UqTehp8x7YiyVxx/38B5XBJxqWi8nVE+SSDZzKB4vI0D2iP/In1gqUcV5gf7nksHmCG0Vt+ESY9FUhEOZ0QYA==',
    'agentID': '61b5efa89ef90206c8541bba'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


**Sample Response Json**

.. code:: json
  
    {
      "success": "success",
      "body": {
        "dataRelation": [
          {
            "brainID": "61937101279636235a1c5c51",
            "columnName": "full_name",
            "brainName": "Gender"
          },
          {
            "brainID": "61deada7fb152c7b9b00f02b",
            "columnName": "utterance",
            "brainName": "Medium Summary"
          },
          {
            "brainID": "61deada7fb152c7b9b00f02b",
            "columnName": "full_name",
            "brainName": "Medium Summary"
          },
          {
            "brainID": "61deada7fb152c7b9b00f02b",
            "columnName": "end_time",
            "brainName": "Medium Summary"
          },
          {
            "brainID": "61deada7fb152c7b9b00f02b",
            "columnName": "start_time",
            "brainName": "Medium Summary"
          },
          {
            "brainID": "619370e3279636235a1c5c4f",
            "columnName": "utterance",
            "brainName": "Aspect"
          },
          {
            "brainID": "61deae54fb152c7b9b00f02c",
            "columnName": "utterance",
            "brainName": "Long Summary"
          },
          {
            "brainID": "61deae54fb152c7b9b00f02c",
            "columnName": "start_time",
            "brainName": "Long Summary"
          },
          {
            "brainID": "61deae54fb152c7b9b00f02c",
            "columnName": "end_time",
            "brainName": "Long Summary"
          },
          {
            "brainID": "61deae54fb152c7b9b00f02c",
            "columnName": "full_name",
            "brainName": "Long Summary"
          },
          {
            "brainID": "6180bc63c7dd291d592f3917",
            "columnName": "utterance",
            "brainName": "Emotion"
          },
          {
            "brainID": "619370a7279636235a1c5c4d",
            "columnName": "utterance",
            "brainName": "Sentiment"
          }
        ]
      }
    }


:Headers: 
    accesskey
    agentID

:Params: 

:Request Body:

:Example Response