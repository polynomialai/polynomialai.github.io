==================
Upload Image
==================

--------------------------------
POST /upload-image
--------------------------------
Upload Image

**Example Request**

.. code:: python

    import requests

    url = "lensservice.polynomial.ai/upload-image"

    payload={}
    files=[
        ('file',('nebula.jpg',open('Pictures/nebula.jpg','rb'),'image/jpeg'))
    ]
    headers = {
        'apikey': '{{apiKey}}',
        'Content-Type': 'multipart/form-data'
    }

    response = requests.request("POST", url, headers=headers, data=payload, files=files)

    print(response.text)

:Headers:     
        apikey

:Body: 
        file (formdata)

:Example Response:

.. code:: json

    {
        "status": 200,
        "message": "eRl5AddwUb3VsHnSFIc6h1VH.jpg uploaded successfully",
        "type": "image/jpeg",
        "lastModified": "2021-11-28T18:21:55.000Z",
        "requestId": "356dadc8-301e-004e-7584-e4f71c000000",
        "size": 1184285,
        "url": "https://polynomialservices.blob.core.windows.net/stores/eRl5AddwUb3VsHnSFIc6h1VH.jpg"
    }