Getting Started With Lens API
=============================

This page will provide you with an excellent introduction to Lens.
Before you begin using Lens, make sure you've completed the installation
instructions.

The code snippets to make a POST request and receive the response are
listed below.

**Python**

.. code:: python

   import requests, json

   url = "http://lensservice.polynomial.ai/kit/analyze"

   payload = {
       "data": [
           {
               "user_id": 1543,
               "full_name": "Aparna Pothanis",
               "email": "aparnna_pothanis@polynomial.ai",
               "name": "Polynomial",
               "utterance": "Hi everyone",
               "identifier": 2,
               "start_time": "2021-10-19 18:00:55.760",
               "end_time": "2021-10-19 18:00:56.780",
           },
           {
               "user_id": 1543,
               "full_name": "Revant Amingad",
               "email": "ramingad@gainsight.com",
               "name": "Gainsight",
               "utterance": " Good afternoon.",
               "identifier": 3,
               "start_time": "2021-10-19 18:00:57.859",
               "end_time": "2021-10-19 18:01:01.250",
           },
       ]
   }

   headers = {"accesskey": "your_agent_key", "agentID": "your_agent_id"}

   response = requests.post(url, headers=headers, data=json.dumps(payload))

   print(response.text, response.status_code)


**cURL**

.. code:: c

   curl --location --request POST 'lensservice.polynomial.ai/kit/analyze' \
  --header 'accesskey: {{key}}' \
  --header 'agentID: 61b5efa89ef90206c8541bba' \
  --data-raw '{

  "data":  [
    {
      "user_id": 1543,
      "full_name": "Aparna Pothanis",
      "email": "aparnna_pothanis@polynomial.ai",
      "name": "Polynomial",
      "utterance": "Hi everyone",
      "identifier": 2,
      "start_time": "2021-10-19 18:00:55.760",
      "end_time": "2021-10-19 18:00:56.780",
  },
    {
      "user_id": 1543,
      "full_name": "Revant Amingad",
      "email": "ramingad@gainsight.com",
      "name": "Gainsight",
      "utterance": "  Good afternoon.",
      "identifier": 3,
      "start_time": "2021-10-19 18:00:57.859",
      "end_time": "2021-10-19 18:01:01.250",
    },
    {<->},
    {<->}
    ]
    }'

**NodeJs - Native**

.. code:: js

   var https = require('follow-redirects').https;
   var fs = require('fs');
    
   var options = {
     'method': 'POST',
     'hostname': 'lensservice.polynomial.ai',
     'path': '/kit/analyze',
     'headers': {
       'accesskey': '{{key}}',
       'agentID': '61b5efa89ef90206c8541bba'
     },
     'maxRedirects': 20
   };
    
   var req = https.request(options, function (res) {
     var chunks = [];
    
     res.on("data", function (chunk) {
       chunks.push(chunk);
     });
    
     res.on("end", function (chunk) {
       var body = Buffer.concat(chunks);
       console.log(body.toString());
     });
    
     res.on("error", function (error) {
       console.error(error);
     });
   });
    
   var postData = '{
       "data":  [
         {
          "user_id": 1543,
          "full_name": "Aparna Pothanis",
          "email": "aparnna_pothanis@polynomial.ai",
          "name": "Polynomial",
          "utterance": "Hi everyone",
          "identifier": 2,
          "start_time": "2021-10-19 18:00:55.760",
          "end_time": "2021-10-19 18:00:56.780",
        },
        {
          "user_id": 1543,
          "full_name": "Revant Amingad",
          "email": "ramingad@gainsight.com",
          "name": "Gainsight",
          "utterance": "  Good afternoon.",
          "identifier": 3,
          "start_time": "2021-10-19 18:00:57.859",
          "end_time": "2021-10-19 18:01:01.250",
        },
       {<->},
       {<->}
    ]
   }'
    
   req.write(postData);
    
   req.end();

**NodeJs - Request**

.. code:: js

   var request = require('request');
   var options = {
     'method': 'POST',
     'url': 'lensservice.polynomial.ai/kit/kit/analyze',
     'headers': {
       'accesskey': '{{key}}',
       'agentID': '61b5efa89ef90206c8541bba'
     },
     body: '{
       "data":  [
         {
          "user_id": 1543,
          "full_name": "Aparna Pothanis",
          "email": "aparnna_pothanis@polynomial.ai",
          "name": "Polynomial",
          "utterance": "Hi everyone",
          "identifier": 2,
          "start_time": "2021-10-19 18:00:55.760",
          "end_time": "2021-10-19 18:00:56.780",
        },
        {
          "user_id": 1543,
          "full_name": "Revant Amingad",
          "email": "ramingad@gainsight.com",
          "name": "Gainsight",
          "utterance": "  Good afternoon.",
          "identifier": 3,
          "start_time": "2021-10-19 18:00:57.859",
          "end_time": "2021-10-19 18:01:01.250",
        },
       {<->},
       {<->}
    ]
   }'
   };
   request(options, function (error, response) {
     if (error) throw new Error(error);
     console.log(response.body);
   });




**Request Parameter**

Sample Request Json

.. code:: json

   {
     "data": [
          {
           "user_id": 1543,
           "full_name": "Aparna Pothanis",
           "email": "aparnna_pothanis@polynomial.ai",
           "name": "Polynomial",
           "utterance": "Hi everyone",
          "identifier": 2,
           "start_time": "2021-10-19 18:00:55.760",
           "end_time": "2021-10-19 18:00:56.780",
         },
         {
           "user_id": 1543,
           "full_name": "Revant Amingad",
           "email": "ramingad@gainsight.com",
           "name": "Gainsight",
           "utterance": "  Good afternoon.",
           "identifier": 3,
           "start_time": "2021-10-19 18:00:57.859",
           "end_time": "2021-10-19 18:01:01.250",
         },
         {<->},
         {<->}
     ]
   }

**Header**

-  accessKey : Unique key provided by the Agent
-  agentID : Unique Id provided by the Agent

**Request Json**

-  identifier : Unique utterance Id
-  start_time : Start time of the utterance
-  end_time : End time of the utterance
-  utterance : Direct Utterance
-  name : Name of the Organisation
-  email : Email id of the speaker
-  full_name : Full name of the speaker
-  user_id : Host of the meeting

**Sample Response Json**

.. code:: json

   {
    "prediction": {
      "genderDistribution": {
        "F": 111,
        "M": 690
      },
      "genderLinguisticInsight": {
        "M": {
          "Accept": 97,
          "Continuer": 47,
          "Emphasis": 3,
          "Greet": 9,
          "Reject": 1,
          "Statement": 479,
          "System": 6,
          "nAnswer": 3,
          "whQuestion": 15,
          "yAnswer": 18,
          "ynQuestion": 12
        },
        "F": {
          "Accept": 7,
          "Continuer": 8,
          "Greet": 1,
          "Statement": 90,
          "yAnswer": 5
        }
      }
    }
   }
   
**Response Json**

-  genderDistribution : Count of Male/Female
-  genderLinguisticInsight : Total count of Linguistic Insights of each
   gender.

**Note:** The response may differ depending on the brains chosen during
agent creation.