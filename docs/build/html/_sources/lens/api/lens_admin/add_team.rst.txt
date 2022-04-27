========
Add Team
========

--------------------------------
POST /add-team
--------------------------------
Add team

**Example Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/add-team"

    payload = {
                "name": "Team 2",
                "users": ["himanshu.t@polynomial.ai"]
            }
    headers = {
    'apikey': '{{apiKey}}'
    }

    response = requests.request("GET", url, headers=headers, data=payload)

    print(response.text)


:Headers:     
      apikey

:Params:


:Request Body:

.. code:: json
    
    {
        "name": "Team 2",
        "users": ["himanshu.t@polynomial.ai"]
    }

:Example Response:

.. code:: json

    {
        "success": "success",
        "body": {
            "teams": [
                {
                    "name": "Team 1",
                    "id": "643839"
                },
                {
                    "name": "Team 2",
                    "id": "643831"
                },
                {
                    "name": "Team 3",
                    "id": "643833"
                },
                {
                    "name": "Team 4",
                    "id": "643834"
                }
            ]
        }
    }   