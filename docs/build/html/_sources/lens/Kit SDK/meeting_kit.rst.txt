==================================
Meeting Kit
==================================
--------------------------------
POST /kit/analyze
--------------------------------

Example Request:

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/kit/analyze"

    payload = "{\n    \"data\": [{\"text\":\"anthony said that this is completely stupid.\"}],\n    \"dry\": false\n}"
    headers = {
    'accesskey': 'U2FsdGVkX1/M1yQDF2jTlOBOP8u+G3CKYJnPPcEHZnF5Woz34aFVQ+bhJvLEBuGLty9l0hNTz8EhhBVfBVaDS7FiQYIVPMa46PE9lJRqCb6gQG3nvkvF/kBviPykcrkwco4w54q562KClo/fJjR379LNZr6MSMvo+0ufCn8Vpi+7M1ZM/j0A5fidkuar6yQSqw9mXeHbeQjOgZHYv9gaM6QEih8J/oM73dmmLR8l8nbKtOEfgxLQ6MD8Xfgl5haF773cEtFxxOTCvbl95ECWgFapsvTwDS3t4nQiL2lGV2TX9w/uTcFpyTiUyozy2k4Jv6arsTDSFbsf12N65v7ghVrVwHLatQ5OG79/yfjFoIQUUpo3c/0jprZ0SDKpFVoQWKSk5I+qvexjET3ah/v1BQ==',
    'agentID': '61d7eaaa486074001f6b2ac9'
    }

    response = requests.request("POST", url, headers=headers, data=payload)

    print(response.text)


:Headers: 
    accesskey
    agentID

:Params: 

:Request Body:
    .. code:: json
        {
        "data": [{"text":"anthony said that this is completely stupid."}],
        "dry": false
    }

:Example Response