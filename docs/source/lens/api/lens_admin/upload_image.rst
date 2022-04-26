Upload Image
==================

**Code snippet for Python Request**

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


**Code snippet for NodeJS Request**

.. code:: js

    var request = require('request');
    var fs = require('fs');
    var options = {
    'method': 'POST',
    'url': 'lensservice.polynomial.ai/upload-image',
    'headers': {
        'apikey': '{{apiKey}}',
        'Content-Type': 'multipart/form-data'
    },
    formData: {
        'file': {
        'value': fs.createReadStream('/Pictures/nebula.jpg'),
        'options': {
            'filename': 'nebula.jpg',
            'contentType': null
        }
        }
    }
    };
    request(options, function (error, response) {
    if (error) throw new Error(error);
    console.log(response.body);
    });

*Example Response*

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